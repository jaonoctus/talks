<script setup lang="ts">
import { ref, computed, onMounted, watchEffect } from 'vue'

const txid = ref('')

const sig1 = ref('5679')
const sig2 = ref('5678')

const isSigValid = (sig, txid, index) => Number(sig) + Number(txid) + Number(index) === 10000

const isFirstSigValid = computed(() => isSigValid(sig1.value, 4321, 0))
const isSecondSigValid = computed(() => isSigValid(sig2.value, 4321, 1))

const sha256 = async (msg) => {
  const msgBuffer = new TextEncoder('utf-8').encode((msg) ? msg : '')

  const hashBuffer = await crypto.subtle.digest('SHA-256', msgBuffer)

  const hashArray = Array.from(new Uint8Array(hashBuffer))

  const hashHex = hashArray.map(b => b.toString(16).padStart(2, '0')).join('')

  return hashHex
}

const updateSig1 = (e) => {
  sig1.value = e.target.innerText
}

watchEffect(async () => {
  const txData = `v1i2o143210${sig1.value}`

  txid.value = await sha256(txData)
})
</script>

<template>
  <div class="mb-6">
    TXID: {{ txid }}
  </div>

  <table class="text-xs border border-collapse" cellspacing="0">
    <tbody>
      <tr>
        <td class="border" colspan="2">
          <span class="highlight">VERSÃO: 1</span>
        </td>
        <td class="border" colspan="2">
          <span class="highlight"> QTD INPUTS: 2 </span>
        </td>
        <td class="border" colspan="2">
          <span class="highlight"> QTD OUTPUTS: 1 </span>
        </td>
      </tr>
      <tr>
        <td class="border text-center" colspan="3">INPUTS</td>
        <td class="border text-center" colspan="3">OUTPUTS</td>
      </tr>
      <tr>
        <td class="border text-center">PREV TXID</td>
        <td class="border text-center">ÍNDICE</td>
        <td class="border text-center">"UNLOCKING SCRIPT"</td>
        <td class="border text-center">QUANTIDADE</td>
        <td class="border text-center" colspan="2">"LOCKING SCRIPT"</td>
        <td class="hidden"></td>
      </tr>
      <tr>
        <td class="border"><span class="highlight">4321</span></td>
        <td class="border"><span class="highlight">0</span></td>
        <td class="border">
          <span class="highlight">
            assinatura jao
            <span
              contenteditable
              v-text="sig1"
              @input="updateSig1"
            ></span>
          </span>
          <mdi-check-circle v-if="isFirstSigValid" class="ml-2 inline text-green-300"/>
          <mdi-close-circle v-else class="ml-2 inline text-red-300"/>
        </td>
        <td class="border" rowspan="2"><span class="highlight">5 BTC</span></td>
        <td class="border" rowspan="2" colspan="2"><span class="highlight">só o narcélio pode gastar</span></td>
        <td class="hidden"></td>
      </tr>
      <tr>
        <td class="border"><span class="highlight">4321</span></td>
        <td class="border"><span class="highlight">1</span></td>
        <td class="border">
          <span class="highlight">
            assinatura satoshi
            <span>{{ sig2 }}</span>
          </span>
          <mdi-check-circle class="ml-2 inline text-green-300"/>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<style scoped>
.highlight {
  @apply border-b border-orange-400;
}
</style>

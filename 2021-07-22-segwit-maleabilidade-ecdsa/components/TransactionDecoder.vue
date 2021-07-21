<script setup lang="ts">
import { ref, computed, watchEffect } from 'vue'
import mempoolJS from '@mempool/mempool.js'

const txId = ref('8dd7162badc8f9780554d06bfeadb5d734eb35c3a157934c80185b8fe9694c4a')

const txHex = ref(null)

// const txData = ref(null)

const hasTxHex = computed(() => txHex.value !== null)

// const hasTxData = computed(() => txData.value !== null)

const reverseBytes = (txt) => txt.match(/[a-fA-F0-9]{2}/g).reverse().join('')

const txHexDetailed = computed(() => {
  const hex = txHex.value

  // 4 bytes
  const versionReverse = hex.substring(0, 8)
  const version = reverseBytes(versionReverse)

  // 1 byte
  const inputCount = hex.substring(8, 10)

  const inputs = []

  for (let inputIndex = 0; inputIndex < inputCount; inputIndex++) {
    // 32 bytes
    const txidReverse = hex.substring(10, 10+64)
    const txid = txidReverse

    inputs.push({
      inputIndex,
      txidReverse,
      txid,
    })
  }

  const data = {
    version,
    versionReverse,
    inputCount,
  }


  return data
})

const setTxHex = async (txid) => {
  const { bitcoin: { transactions } } = mempoolJS()

  txHex.value = await transactions.getTxHex({ txid })
  // txData.value = await transactions.getTx({ txid })
}

watchEffect(async () => {
  await setTxHex(txId.value)
})

</script>

<template>
  <label>TXID:</label>
  <input
    v-model="txId"
    class="w-full bg-gray-600 rounded p-1 my-2"
  />

  <div class="grid grid-cols-1 gap-4">
    <div>
      <div>HEX</div>
      <div v-if="hasTxHex" class="bg-gray-600 rounded p-1 my-2 break-all">
        <span class="bg-purple-400" :title="`Versão ${txHexDetailed.version}`">{{ txHexDetailed.versionReverse }}</span>
        <span class="bg-orange-400" title="Quantidade de inputs">{{ txHexDetailed.inputCount }}</span>
        <span v-for="input in txHexDetailed.inputs" :key="input.inputIndex">
          <span class="bg-orange-400" title="Quantidade de inputs">{{ txHexDetailed.inputCount }}</span>
        </span>
      </div>
    </div>
  </div>
</template>

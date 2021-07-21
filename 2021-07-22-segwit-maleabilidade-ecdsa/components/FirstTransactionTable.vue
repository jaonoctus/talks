<script setup lang="ts">
</script>

<template>
  <div class="mb-6">
    TXID:
      <span class="text-purple-400">
        sha256(
          <span class="text-blue-400">
            sha256(
              <span class="text-orange-500">conteúdo da transação</span>
            )
          </span>
        )
      </span>
    = 4321
  </div>

  <table class="text-xs border border-collapse" cellspacing="0">
    <tbody>
      <tr>
        <td class="border" colspan="2">
          <span class="highlight">VERSÃO: 1</span>
        </td>
        <td class="border" colspan="2">
          <span class="highlight"> QTD INPUTS: 1 </span>
        </td>
        <td class="border" colspan="2">
          <span class="highlight"> QTD OUTPUTS: 2 </span>
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
        <td class="border" rowspan="2"><span class="highlight">1234</span></td>
        <td class="border" rowspan="2"><span class="highlight">0</span></td>
        <td class="border" rowspan="2">
          <span class="highlight">assinatura 8766</span>
        </td>
        <td class="border"><span class="highlight">3 BTC</span></td>
        <td class="border" colspan="2"><span class="highlight">só o jão pode gastar</span></td>
        <td class="hidden"></td>
      </tr>
      <tr>
        <td class="border"><span class="highlight">3 BTC</span></td>
        <td class="border" colspan="2"><span class="highlight">só o satoshi pode gastar</span></td>
        <td class="hidden"></td>
      </tr>
    </tbody>
  </table>
</template>

<style scoped>
.highlight {
  @apply border-b border-orange-400;
}
</style>

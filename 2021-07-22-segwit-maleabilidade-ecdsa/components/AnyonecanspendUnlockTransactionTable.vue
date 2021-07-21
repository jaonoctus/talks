<template>
  <div class="mb-6">
    TXID: da2876b3eb31edb4436fa4650673fc6f01f90de2f1793c4ec332b2387b09726f
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
        <td class="border"><span class="highlight">4ny0n3...</span></td>
        <td class="border"><span class="highlight">0</span></td>
        <td class="border"></td>
        <td class="border"><span class="highlight">10 BTC</span></td>
        <td class="border" colspan="2"><span class="highlight">OP_DUP OP_HASH160 OP_PUSHBYTES_20 ... OP_EQUALVERIFY OP_CHECKSIG</span></td>
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

<template>
  <div class="mb-6">
    TXID: 4ny0n3...
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
        <td class="border"><span class="highlight">9876</span></td>
        <td class="border"><span class="highlight">3</span></td>
        <td class="border">
          <span class="highlight">
            assinatura 124
          </span>
        </td>
        <td class="border"><span class="highlight">10 BTC</span></td>
        <td class="border" colspan="2"><span class="highlight">qualquer um pode gastar (OP_TRUE)</span></td>
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

<script setup lang="ts">
import { computed } from 'vue'

const txid = computed(() => {
  return '1234'
})

</script>

<template>
  <div class="grid grid-cols-2 gap-4">
    <div class="col-span-2">

      <div class="flex">
        <div class="bg-gray-400 p-2">TXID</div>
        <div class="bg-orange-700 p-2">{{ txid }}</div>
      </div>

    </div>
    <div>
      Inputs
      <div class="border">
        txid:
        <br>
        <input class="bg-gray-600 w-full"/>
        <br><br>
        index:
        <br>
        <input class="bg-gray-600"/>
        <br><br>
        assinatura:
        <br>
        <input class="bg-gray-600"/>
      </div>
    </div>
    <div>
      Outputs
      <div class="border">
        script:
        <br>
        <input class="bg-gray-600 w-full"/>
        <br><br>
        amount:
        <br>
        <input class="bg-gray-600" value="8.00000000"/>
      </div>
      <div class="border mt-5">
        script:
        <br>
        <input class="bg-gray-600 w-full" value="76a9146c8de651f8b92f87ff43fb9732babec784bdb6f588ac"/>
        <br><br>
        amount:
        <br>
        <input class="bg-gray-600" value="1.00000000"/>
      </div>
    </div>
  </div>
</template>

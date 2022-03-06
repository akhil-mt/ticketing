<script setup>
const props = defineProps(["lt", "ticketNo", "counterNo"]);
</script>

<template>
  <div
    class="flex rounded-lg shadow-lg my-4 mx-4 border bg-blue-500 overflow-hidden"
    :class="[props && props.lt ? 'bg-green-500' : '']"
  >
    <div class="w-3/5 text-center">
      <div class="py-2 pt-4 text-md text-white uppercase tracking-wider">
        Ticket No
      </div>
      <div class="text-5xl pb-6 font-bold text-white uppercase">
        {{ props.ticketNo }}
      </div>
    </div>
    <div
      class="w-2/5 text-center bg-blue-400"
      :class="[props && props.lt ? 'bg-green-400' : '']"
    >
      <div class="py-2 pt-4 text-md text-white uppercase tracking-wider">
        Counter
      </div>
      <div class="text-5xl pb-6 font-bold text-white uppercase">
        {{ props.counterNo }}
      </div>
    </div>
  </div>
</template>

<style></style>

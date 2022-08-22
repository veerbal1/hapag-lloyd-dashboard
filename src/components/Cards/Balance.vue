<template>
  <div class="w-full h-48 shadow-md p-6">
    <h1 class="text-2xl antialiased font-normal">Balance</h1>
    <h1 class="text-4xl antialiased font-normal mb-2">
      &euro; {{(224466).toLocaleString()}}
    </h1>
    <h6 class="text-sm font-thin">Average Monthly</h6>
    <h6 class="text-sm font-thin">&euro; {{(336699).toLocaleString()}}</h6>
  </div>
</template>

<script>
export default {
  name: 'BalanceCard'
}
</script>

<style>
</style>
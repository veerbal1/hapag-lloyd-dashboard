<template>
  <div class="w-full max-w-xs shadow-md p-6">
    <h1 class="text-xl antialiased font-normal">{{ title }}</h1>
    <h1 class="text-4xl antialiased font-normal mb-2">
      {{ value }}
    </h1>
    <h6 class="text-sm font-thin">{{ secondaryTitle }}</h6>
    <h6 class="text-sm font-thin">&euro; {{ secondaryValue }}</h6>
  </div>
</template>

<script>
export default {
  name: 'BalanceCard',
  props: ["title", "value", "secondaryTitle", "secondaryValue"],
  data() {
    return {
      currentBalance: 312312,
      averageBalance: 336699
    }
  }
}
</script>

<style>
</style>
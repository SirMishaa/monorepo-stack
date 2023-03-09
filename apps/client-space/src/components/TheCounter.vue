<script setup lang="ts">
const properties = defineProps<{
  initial: number
}>()

const { count, inc, dec } = useCounter(properties.initial)
</script>

<template>
  <div>
    {{ count }}
    <button class="inc" @click="inc()">+</button>
    <button class="dec" @click="dec()">-</button>
  </div>
</template>

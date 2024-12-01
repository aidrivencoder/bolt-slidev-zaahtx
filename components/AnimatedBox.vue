<script setup lang="ts">
const props = defineProps({
  initial: {
    type: Object,
    default: () => ({ x: 0, y: 0 }),
  },
  enter: {
    type: Object,
    default: () => ({ x: 0, y: 0 }),
  },
})
</script>

<template>
  <div
    v-motion
    :initial="initial"
    :enter="enter"
    class="w-32 h-32 bg-blue-500 rounded-lg"
  />
</template>
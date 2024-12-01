<script setup lang="ts">
const props = defineProps({
  text: {
    type: String,
    required: true
  },
  initial: {
    type: Object,
    default: () => ({ opacity: 0, y: 100 }),
  },
  enter: {
    type: Object,
    default: () => ({ opacity: 1, y: 0 }),
  },
})
</script>

<template>
  <h2
    v-motion
    :initial="initial"
    :enter="enter"
    class="text-2xl font-bold"
  >
    {{ text }}
  </h2>
</template>
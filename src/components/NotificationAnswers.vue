<script setup>
const props = defineProps({
  correct: {
    required: true,
  },
})
</script>

<template>
  <div
    class="notification"
    :class="props.correct ? 'bg-blue-500' : 'bg-red-500'"
  >
    {{ props.correct ? 'Correct' : 'Wrong' }}
  </div>
</template>

<style lang="postcss" scoped>
.notification {
  @apply absolute inset-0 flex items-center justify-center text-8xl font-bold uppercase tracking-widest text-white;
}
</style>
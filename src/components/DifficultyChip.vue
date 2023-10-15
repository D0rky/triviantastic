<script setup>
const props = defineProps({
  difficulty: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <p
    class="difficulty"
    :class="
      props.difficulty === 'easy'
        ? 'bg-green-600'
        : props.difficulty === 'medium'
        ? 'bg-yellow-600'
        : 'bg-red-500'
    "
  >
    {{ props.difficulty }}
  </p>
</template>

<style lang="postcss" scoped>
.difficulty {
  @apply absolute bottom-2 left-2 rounded-full bg-blue-400 px-4 py-1 text-sm font-bold capitalize text-slate-800;
}
</style>
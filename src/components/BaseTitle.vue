<template>
  <div class="brand">
    <slot name="logo" />
    <h1 class="title">
      <slot />
    </h1>
    <slot name="logo" />
  </div>
</template>

<style lang="postcss" scoped>
.brand {
  @apply flex items-center justify-center gap-4;

  & :slotted(img) {
    @apply h-16 w-16;
  }

  & .title {
    @apply text-center text-5xl font-semibold tracking-widest text-slate-700;
  }
}
</style>
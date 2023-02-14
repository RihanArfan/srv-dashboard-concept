<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    type?: "button" | "a";
    block?: boolean;
  }>(),
  {
    type: "button",
  }
);
</script>

<template>
  <button
    v-if="type === 'button'"
    type="button"
    class="rounded-full bg-neutral-900 py-3 px-7 font-semibold text-white transition-colors hover:bg-neutral-700 dark:bg-neutral-100 dark:text-black dark:hover:bg-neutral-300"
    :class="{ 'w-full': block }"
  >
    <slot />
  </button>

  <NuxtLink
    v-else
    class="block rounded-full bg-neutral-900 py-3 px-7 font-semibold text-white transition-colors hover:bg-neutral-700 dark:bg-neutral-100 dark:text-black dark:hover:bg-neutral-300"
    :class="{ 'w-full': block }"
  >
    <slot />
  </NuxtLink>
</template>

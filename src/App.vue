<script setup lang="ts">
import { useDark, useToggle } from "@vueuse/core";
import ChildText from "@/components/ChildText.vue";

const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>

<template>
  <h1 class="text-green-700 dark:text-green-300">Hello</h1>
  <button
    class="text-black dark:text-white rounded shadow-sm ring-1 ring-inset ring-gray-300 dark:ring-slate-700 hover:bg-gray-100 dark:hover:bg-black p-4"
    @click="toggleDark()"
  >
    Dark: {{ isDark }} , click to change
  </button>
  <span class="block classic-apply">this is the target of an @apply rule</span>
  <div class="wrapper">
    <ChildText />
  </div>
</template>

<style scoped>
.classic-apply {
  @apply text-xl text-orange-700 dark:text-white;
}

.wrapper :deep(.child-text) {
  @apply text-pink-700 dark:text-yellow-300;
}
</style>

<style>
.wrapper .child-text-global {
  @apply text-sky-700 dark:text-purple-300;
}
</style>

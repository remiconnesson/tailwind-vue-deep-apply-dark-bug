<script setup lang="ts">
import { useDark, useToggle } from "@vueuse/core";
const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>

<template>
  <h1 class="text-green-700 dark:text-green-300">Hello</h1>
  <button class="text-black dark:text-white rounded shadow-sm ring-1 ring-inset ring-gray-300 dark:ring-slate-700 hover:bg-gray-100 dark:hover:bg-slate-950 p-4" @click="toggleDark()">
    Dark: {{ isDark }} , click to change
  </button>
  <span class="block classic-apply">this is the target of an @apply rule</span>
</template>

<style scoped>
.classic-apply {
  @apply text-xl text-orange-700 dark:text-white
}
</style>

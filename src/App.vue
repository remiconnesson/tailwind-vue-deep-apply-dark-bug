<script setup lang="ts">
import { useDark, useToggle } from "@vueuse/core";
const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>

<template>
  <h1 class="text-green-700 dark:text-green-300">Hello</h1>
  <button class="text-black dark:text-white" @click="toggleDark()">
    Dark: {{ isDark }}
  </button>
</template>

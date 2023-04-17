<template>
  <div class="child-text text-xl mt-8">
    I am targeted by my parent component with
  </div>
  <pre class="block child-pre text-black dark:text-white">
&lt;style scoped&gt;
.wrapper :deep(.child-text) {
  @apply text-pink-700 dark:text-yellow-300
}
&lt;/style&gt;
  </pre>

  <div class="child-text-global text-xl mt-8">
    I am targeted by my parent component with
  </div>
  <pre class="block child-pre text-black dark:text-white">
&lt;style&gt;
.child-text-global {
  @apply text-sky-700 dark:text-purple-300
}
&lt;/style&gt;
  </pre>
</template>

<style scoped></style>

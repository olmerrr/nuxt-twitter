<template>
  <div class="m-2 border rounded-2xl bg-gray-50 dark:bg-dim-700" :class="twitterBorderColor">
    <h1 class="p-3 text-xl font-extrabold text-gray-900 border-b dark:text-white">
      {{props.title}}
    </h1>
    <slot></slot>
    <div class="p-3 text-sm text-blue-400 cursor-pointer hover:bg-gray-50">Show more</div>
  </div>
</template>

<script setup>
  import useTailwindConfig from "~/composables/useTailwindConfig.js";

  const props = defineProps({
    title: {
      type: String,
      required: true
    }
  });
  const {twitterBorderColor} = useTailwindConfig();
</script>
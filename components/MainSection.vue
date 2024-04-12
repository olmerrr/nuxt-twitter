<template>
  <div class="border-x">
    <div class="sticky top-0 px-4 py-3 bg-white/80 backdrop-blur-md dark:bg-dim-900/80">
      <h2 class="text-xl font-bold text-gray-800 dark:text-gray-100">{{ title }}</h2>
    </div>
    <div
        class="loading flex justify-center p-4 border-b"
        :class="twitterBorderColor"
         v-if="loading">
      <UISpinner />
    </div>

    <div class="content" v-else>
      <slot></slot>
    </div>
  </div>
</template>
<script setup>
  import useTailwindConfig from "~/composables/useTailwindConfig.js";

  const props = defineProps({
    title: {
      type: String,
      required: true
    },
    loading: {
      type: Boolean,
      required: true,
    }
  })
  const {defaultTransition, twitterBorderColor} = useTailwindConfig();
</script>
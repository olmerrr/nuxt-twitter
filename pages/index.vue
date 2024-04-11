<template>
  <div :class="{'dark': darkMode}">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <div class="grid grid-cols-12 mx-auto sm:px-6 lx:max-w-7xl lg:px-8 lg:gap-10">

          <!--left sidebar-->
          <div class="hidden md:block xs-col-span-1 xl:col-span-2">
            <div class="sticky top-0">
              <SidebarLeft />
            </div>
          </div>
          <!--left sidebar-->

          <!--main content-->
<!--          <main class="col-span-12 md:col-span-8 xl:col-span-6 bg-red-400">-->
<!--            main-->
<!--          </main>-->
          <!--main content-->

          <!--right sidebar-->
          <div class="col-span-12 md:block xl:col-span-4 md:col-span-3 bg-blue-300">
            <div class="sticky top-0">
              <SidebarRight />
            </div>
          </div>
          <!--right sidebar-->
        </div>
        <button @click="darkMode = !darkMode" class="dark:text-white border border-red-600 bg-green-500">Theme switcher</button>

      </div>

    </div>

  </div>
</template>

<script setup lang="ts">
const darkMode = ref(false);
</script>
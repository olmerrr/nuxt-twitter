<template>
  <div class="h-screen flex flex-col">
    <div class="p-2 my-2 rounded-full hover:bg-blue-50 w-min dark:hover:bg-white/20" :class="defaultTransition">
      <nuxt-link to="/">
        <div class="w-8 h-8">
          <LogoTwitter/>
        </div>
      </nuxt-link>
    </div>

    <div class="mt-2 space-y-3">
      <SidebarLeftTab >
        <template v-slot:icon>
          <HomeIcon/>
        </template>
        <template v-slot:name>
          Home
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <HashtagIcon/>
        </template>
        <template v-slot:name>
          Explore
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <InboxIcon/>
        </template>
        <template v-slot:name>
          Messages
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <BookmarkIcon/>
        </template>
        <template v-slot:name>
          Bookmarks
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab >
        <template v-slot:icon>
          <DocumentTextIcon/>
        </template>
        <template v-slot:name>
          Lists
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <UserIcon/>
        </template>
        <template v-slot:name>
          Profile
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <AcademicCapIcon/>
        </template>
        <template v-slot:name>
          More
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <BellIcon/>
        </template>
        <template v-slot:name>
          Notification
        </template>
      </SidebarLeftTab>
    </div>
  </div>
</template>

<script setup>
import { HomeIcon, HashtagIcon, BellIcon,   InboxIcon, BookmarkIcon, DocumentTextIcon, UserIcon, AcademicCapIcon } from "@heroicons/vue/16/solid/index.js";

import useTailwindConfig from "~/composables/useTailwindConfig.js";

const { defaultTransition } = useTailwindConfig();
const isActive = ref(true);
</script>
<template>
  <div class="flex flex-col">
    <SidebarRightPreviewCard title="Whats happening">
      <SidebarRightPreviewCardItem
          v-for="whatsHappened in whatsHappenedItems"
          :key="whatsHappened.title">
        <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatsHappened.title }}</h2>
        <p class="text-xs text-gay-400">{{ whatsHappened.count }}</p>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>

    <SidebarRightPreviewCard title="Who to follow">
      <SidebarRightPreviewCardItem
          v-for="whoToFollow in whoToFollowItems"
          :key="whoToFollow.name">
        <div class="flex flex-row justify-between p-2">
          <div class="flex flex-row">
            <img
                :src="whoToFollow.image"
                :alt="whoToFollow.name"
                class="w-10 h-10 rounded-full"
            />
            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 :dark:text-white">{{ whoToFollow.name }}</h1>
              <p class="">{{ whoToFollow.handle }}</p>
            </div>
          </div>
        </div>

      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>


  </div>
</template>
<script setup lang="ts">
const whatsHappenedItems = ref([
  {
    title: "Space X",
    count: "18.8k Tweets"
  },
  {
    title: "Microsoft",
    count: "28.3k Tweets"
  },
  {
    title: "Facebook",
    count: "12.8k Tweets"
  },
]);
const whoToFollowItems = ref([
  {
    name: "John Makefile",
    handle: "@johnMake",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Ketty Onyx",
    handle: "@kettyOnyx"
  },
  {
    name: "Matt Bree",
    count: "@breeM"
  },
]);
</script>
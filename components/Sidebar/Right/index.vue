<template>
  <div class="flex flex-col">
    <SidebarRightPreviewCard title="Whats happening">
      <SidebarRightPreviewCardItem
          v-for="whatsHappened in whatsHappenedItems"
          :key="whatsHappened.title">
        <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatsHappened.title }}</h2>
        <p class="text-xs text-gay-400 dark:text-white">{{ whatsHappened.count }}</p>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>

    <SidebarRightPreviewCard title="Who to follow">
      <SidebarRightPreviewCardItem
          v-for="(whoToFollow, index) in whoToFollowItems"
          :key="whoToFollow.name">
        <div class="flex items-center flex-row justify-between p-2">
          <div class="flex flex-row">
            <img
                :src="generateImageURL(index+ 1)"
                :alt="whoToFollow.name"
                class="w-10 h-10 rounded-full"
            />
            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whoToFollow.name }}</h1>
              <p class="text-xs text-gray-400 dark:text-white">{{ whoToFollow.handle }}</p>
            </div>
          </div>
          <div class="flex h-full">
            <button class="px-4 py-2 text-xs font-bold text-white dark:text-black bg-black dark:bg-white rounded-full">
              Follow
            </button>
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
  },
  {
    name: "Ketty Onyx",
    handle: "@kettyOnyx",

  },
  {
    name: "Matt Bree",
    handle: "@breeM",
  },
]);

const generateImageURL = (index: number): string => {
  return `https://picsum.photos/seed/${index}/200/200`;
};
</script>
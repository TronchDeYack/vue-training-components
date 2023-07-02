<script lang="ts" setup>
interface Stats {
  followers: number
  following: number
  projects: number
}
defineProps<{
  name: string,
  job: string,
  description: string,
  stats: Stats,
  avatar: string,
}>()
</script>

<template>
  <div class="p-2 rounded-2xl bg-white max-w-lg">
    <div class="px-4 pt-2 pb-6 flex flex-col sm:flex-row bg-gray-50">
      <img :src="avatar" class="profile-img rounded-full w-32 h-32 border-4 border-gray-300 object-cover sm:flex-none flex-1">
      <div class="ml-4">
        <h1 class="text-2xl font-medium">{{ name }}</h1>
        <div class="text-gray-500">{{ job }}</div>
        <div class="mt-1">{{ description }}</div>

        <div class="mt-6 flex flex-col sm:flex-row space-y-2 sm:space-y-0 sm:space-x-6 text-sm">
          <div class="flex-1 text-center">
            <div>{{ stats.followers }}</div>
            <div>Followers</div>
          </div>
          <div class="flex-1 text-center">
            <div>{{ stats.following }}</div>
            <div>Following</div>
          </div>
          <div class="flex-1 text-center">
            <div>{{ stats.projects }}</div>
            <div>Projects</div>
          </div>
        </div>

        <div class="flex space-x-4 mt-6">
          <button class="p-2 bg-cyan-300 hover:bg-cyan-200 flex-1 rounded-lg border border-black transition-colors duration-200">Follow</button>
          <button class="p-2 bg-yellow-300 hover:bg-yellow-200 flex-1 rounded-lg border border-black transition-colors duration-200">View Profile</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="postcss" scoped>
.profile-img {
  max-width: 128px;
  max-height: 128px;
}
</style>
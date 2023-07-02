<script setup lang="ts">
import ProfileCard from './components/ProfileCard.vue'

</script>

<template>
  <main class="w-full h-full">
    <ProfileCard 
      name="John Doe"
      avatar="https://picsum.photos/id/237/200/300"
      job="Frontend developer"
      description="Passionate frontend developer with expertise in HTML, CSS, Javascript and VueJS."
      :stats="{
        followers: 1999,
        following: 190,
        projects: 15,
      }"
    />
  </main>
</template>

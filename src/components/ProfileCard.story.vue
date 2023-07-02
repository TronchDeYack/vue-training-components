<script setup lang="ts">
import ProfileCard from './ProfileCard.vue'
</script>

<template>
  <Story>
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
  </Story>
</template>
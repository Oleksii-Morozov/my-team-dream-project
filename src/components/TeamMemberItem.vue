<script setup lang='ts'>
import type { TeamMember } from '@/shared/types';

defineProps<{
  teamMember: TeamMember;
}>()
</script>

<template>
  <main>
    <h1>{{ teamMember.name }}</h1>
    <p>{{ teamMember.position }}</p>
    <img :src='teamMember.image' :alt='teamMember.name' />
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: left;
  padding: 0 1rem;
  max-width: 15rem;
}

h1 {
  font-size: 1.5rem;
  margin: 0;
}

p {
  font-size: 1rem;
  margin: 0;
}

img {
  border-radius: 50%;
  width: 15rem;
  aspect-ratio: 1 / 1;
}

</style>

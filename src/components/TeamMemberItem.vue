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
  background-color: var(--color-background-mute);
  border-radius: 1rem;
  padding: 1.5rem;
  width: 18rem;
  transition: scale .3s ease-in-out;
  text-align: center;
}

main:hover {
  background-color: var(--color-background-soft);
  scale: 1.05;
}


h1 {
  font-size: 1.5rem;
  margin: 0;
  color: var(--color-heading);
}

p {
  font-size: 1rem;
  margin: 0;
  color: var(--color-text);
}

img {
  border-radius: 50%;
  width: 12rem;
  aspect-ratio: 1 / 1;
  padding: 1rem;
}

</style>

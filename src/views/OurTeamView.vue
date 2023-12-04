<script setup lang="ts">
import TeamMemberItem from '@/components/TeamMemberItem.vue';
import type { TeamMember } from '@/shared/types';

const teamMembers: TeamMember[] = [
  {
    id: 1,
    name: 'Oleksii Morozov',
    position: 'Project Manager',
    image: 'https://avatars.githubusercontent.com/u/95098796?v=4',
  }
];

</script>

<template>
  <main v-for='teamMember in teamMembers' :key='teamMember.id'>
    <TeamMemberItem :teamMember=teamMember />
  </main>
</template>

<style scoped>

main {
  display: flex;
  flex-direction: column;
  align-items: left;
  justify-content: flex-start;
  height: 100vh;
  padding: 2rem 2rem;
}

</style>

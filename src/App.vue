<script setup lang="ts">
import TeamMemberItem from '@/components/TeamMemberItem.vue';
import SideElement from './components/SideElement.vue';
import type { TeamMember } from '@/shared/types';

const teamMembers: TeamMember[] = [
  {
    id: 1,
    name: 'Oleksii Morozov',
    position: 'Project Manager',
    image: 'https://avatars.githubusercontent.com/u/95098796?v=4',
  }, 
  {
    id: 2,
    name: 'Albert Rudenko',
    position: 'Frontend Developer',
    image: 'https://avatars.githubusercontent.com/u/31893948?v=4',
  }
];
</script>

<template>
  <main class="root">
    <div class="text">
      <SideElement text='Our brave team' />
    </div>
    <div class="members">
      <div v-for='teamMember in teamMembers' :key='teamMember.id'>
        <TeamMemberItem :teamMember=teamMember />
      </div>
    </div>
  </main>
</template>

<style scoped>
.root {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 5rem;
}
.text {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 5rem;
  flex-wrap: wrap;
}
.members {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 45rem;
  gap: 1rem;
}
</style>

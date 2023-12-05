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
  }, {
    id: 2,
    name: 'Roman Nikitin',
    position: 'Developer',
    image: 'https://i.imgur.com/QVy6Iu0.png',
  },
  {
    id: 3,
    name: 'Ihor Paranchuk',
    position: 'Quality assurance',
    image: 'https://imgur.com/3Ztlpuc.png',
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

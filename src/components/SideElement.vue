<script setup lang='ts'>

defineProps<{
  text: string;
}>()
</script>

<template>
  <main class="text">
    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg"/> -->
    <h1>{{ text }}</h1>
  </main>
</template>

<style scoped>
.logo {
  width: 5rem;
  aspect-ratio: 1 / 1;
  margin-right: 1rem;
}
.text {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: var(--color-background-mute);
  border-radius: 1rem;
  padding: 1rem;
  width: 25rem;
  height: 10rem;
}
</style>

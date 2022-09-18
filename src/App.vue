<script setup lang="ts">
  import PageBackground from './components/PageBackground.vue';
  import DateTime from './components/DateTime.vue';
  import SearchBar from './components/SearchBar.vue';
  import LinksBar from './components/LinksBar.vue';
</script>

<template>
  <PageBackground />
  <div class="wrapper">
    <div class="items">
      <LinksBar />
      <SearchBar />
      <DateTime />
    </div>
  </div>
</template>

<style scoped>
  .wrapper {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
    justify-content: center;
    align-items: center;
  }
  .items {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 1em;
  }
</style>

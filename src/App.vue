<script setup lang="ts">
  import PageBackground from './components/PageBackground.vue';
  import DateTime from './components/DateTime.vue';
</script>

<template>
  <PageBackground />
  <div class="wrapper">
    <DateTime />
  </div>
</template>

<style scoped>
  .wrapper {
    display: flex;
    width: 100%;
    height: 100%;
    justify-content: center;
    align-items: center;
  }
</style>

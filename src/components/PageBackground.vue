<template>
  <video autoplay muted loop>
    <source src="../assets/video.mp4" type="video/mp4" />
  </video>
</template>

<style scoped>
  video {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
</style>

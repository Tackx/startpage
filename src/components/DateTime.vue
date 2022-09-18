<template>
  <div class="datetime">
    <span>{{ weekday }}</span>
    <span>{{ date }}</span>
    <span>{{ time }}</span>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    data() {
      return {
        weekday: '',
        date: '',
        time: ''
      };
    },
    mounted() {
      this.setDate();
      this.setTime();
      setInterval(this.setTime, 1000);
    },
    methods: {
      setDate() {
        const today = new Date();
        const weekday = today.toLocaleDateString(undefined, { weekday: 'long' });
        const month = today.toLocaleDateString(undefined, { month: 'long' });
        const day = today.getDate();
        const year = today.getFullYear();
        this.weekday = weekday;
        this.date = day + ' ' + month + ' ' + year;
      },
      setTime() {
        const now = new Date();
        const hours = now.getHours() < 10 ? '0' + now.getHours() : now.getHours();
        const minutes = now.getMinutes() < 10 ? '0' + now.getMinutes() : now.getMinutes();
        this.time = hours + ':' + minutes;
      }
    }
  });
</script>

<style scoped>
  video {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    min-height: 100%;
  }
</style>

<template>
  <div class="app" id="app">
    <CircleSlider />
  </div>
</template>

<script>
import CircleSlider from "@/components/CircleSlider";

export default {
  name: 'App',
  components: {
    CircleSlider,
  }
}
</script>

<style>
body {
  background-color: black;
}
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 1200px;
}
</style>

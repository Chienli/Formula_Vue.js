<template>
  <div id="app">
    <div class="view">
      <div class="container">
        <Box :key="number" v-for="number in array" :number="number" />
      </div>
    </div>
  </div>
</template>

<script>
import Box from "./components/Box.vue";

export default {
  name: "app",
  data: () => ({
    array: [1, 2, 3, 4, 5, 6, 7, 8, 9]
  }),
  components: {
    Box
  }
};
</script>

<style scoped>
.view {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.container {
  width: 1280px;
  height: 1372px;
  background-color: #eeeeee;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
}
</style>

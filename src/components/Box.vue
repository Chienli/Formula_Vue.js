<template>
  <div class="box">
    <div class="col">
      <div class="number">{{number}}</div>
      <div
        class="formula"
        :key="value"
        v-for="value in a"
      >{{number}} × {{value}} = {{number * value}}</div>
    </div>
    <div class="col">
      <div
        class="formula"
        :key="value"
        v-for="value in b"
      >{{number}} × {{value}} = {{number * value}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Box",
  data: () => ({
    a: [1, 2, 3],
    b: [4, 5, 6, 7, 8, 9]
  }),
  props: ["number"]
};
</script>

<style scoped>
.box {
  width: 350px;
  height: 366px;
  background-color: white;
  border-radius: 100px 0 30px 0;
  box-shadow: 0 3px 10px;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
.number {
  font-size: 128px;
  height: 115px;
  line-height: 115px;
  font-family: "Helvetica";
  font-weight: bold;
  text-shadow: 4px 3px 0xp;
  color: #2eb738;
}
.col {
  height: 238px;
  width: 105px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}
.formula {
  font-family: "Helvetica";
  font-size: 22px;
  color: #2eb738;
  width: 105px;
}
</style>

<template>
  <div id="app" :style="`background-color: rgb(${red}, ${green}, ${blue})`">
    <div class="input-wrapper">
      <input v-model="red" />
      <input v-model="green" />
      <input v-model="blue" />
    </div>
    <div class="input-wrapper">
      <input type="range" v-model="red" />
      <input type="range" v-model="green" />
      <input type="range" v-model="blue" />
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    red: 0,
    green: 0,
    blue: 0
  })
};
</script>

<style>
html, body {
  height: 100px;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: black;
  padding: 10px;
  height: 1000px;
  width: 1000px;
  display: flex;
  flex-direction: row;
}

.input-wrapper {
  display: flex;
  flex-direction: column;
  max-width: 5vw;
}
</style>

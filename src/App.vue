<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.row {
    background-color: aliceblue;
    /* border-radius: 15px; 
    box-shadow: 0px 0px 6px #888;*/
    border-color: black;
}
.col {
    background-color: aliceblue;
    /* border-radius: 15px;
    box-shadow: 0px 0px 6px #888;*/
    border-color: black;
}
</style>

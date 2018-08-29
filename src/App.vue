<template>
  <div id="app">
    <!-- <img src="./assets/logo.png">
    <HelloWorld/> -->
    <Header/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import Header from './components/Header'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Header
  }
}
</script>

<style lang="scss">
@import "../src/assets/styles/main"
// #app {
//   font-family: 'Avenir', Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
//   margin-top: 60px;
// }
</style>

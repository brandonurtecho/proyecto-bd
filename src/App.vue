<template>
  <div id="app">
    <!-- <img src="./assets/logo.png">
    <HelloWorld/> -->   
    <div class="body__container">
      <Header/>
      <carousel/>
      <ReleaseSection/>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import Header from "./components/Header";
import Carousel from "./components/Carousel";
import ReleaseSection from "./components/ReleaseSection";

export default {
  name: "App",
  components: {
    // HelloWorld
    Header,
    Carousel,
    ReleaseSection
  }
};
</script>

<style lang="scss">
@import "../src/assets/styles/main";
// #app {
//   font-family: 'Avenir', Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
//   margin-top: 60px;
// }
#app {
  display: flex;
  justify-content: center;
  .body__container {
    width: 70%;
  }
}
</style>

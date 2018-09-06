<template>
  <div id="app">
    <!-- <img src="./assets/logo.png">
    <HelloWorld/> -->   
    <div class="body__container">
      <Header/>
      <carousel/>
      <WelcomeSection/>
      <AboutSection/>
      <InfoSection/>
      <Footer/>
      <!-- <ReleaseSection/> -->
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import Header from "./components/Header";
import Carousel from "./components/Carousel";
import WelcomeSection from "./components/WelcomeSection";
import InfoSection from "./components/InfoSection";
import AboutSection from "./components/AboutSection";
import Footer from "./components/Footer";
import ReleaseSection from "./components/ReleaseSection";


export default {
  name: "App",
  components: {
    // HelloWorld
    Header,
    Carousel,
    WelcomeSection,
    InfoSection,
    AboutSection,
    Footer,
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
    width: 100%;
  }
}
</style>

<template>
  <div id="app">
    <!-- <img src="./assets/logo.png">
    <HelloWorld/> -->   
    <div class="body__container">
      <Header/>
      <carousel/>
      <DestacadoSection class="DestacadoSection" :destacadoData="destacadoData.anime"/>
      <DestacadoSection class="DestacadoSection" :destacadoData="destacadoData.videojuego"/>
      <DestacadoSection class="DestacadoSection" :destacadoData="destacadoData.serie"/>
      <DestacadoSection class="DestacadoSection" :destacadoData="destacadoData.pelicula"/>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import Header from "./components/Header";
import Carousel from "./components/Carousel";
import DestacadoSection from "./components/DestacadoSection";

export default {
  name: "App",
  components: {
    // HelloWorld
    Header,
    Carousel,
    DestacadoSection
  },
  data() {
    return {
      destacadoData: {
        anime: {
          title: "ANIME",
          images: {
            img_1: "../../static/images/img_1.jpg",
            img_2: "../../static/images/img_1.jpg",
            img_3: "../../static/images/img_1.jpg"
          }
        },
        videojuego: {
          title: "VIDEOJUEGOS",
          images: {
            img_1: "../../static/images/img_1.jpg",
            img_2: "../../static/images/img_1.jpg",
            img_3: "../../static/images/img_1.jpg"
          }
        },
        serie: {
          title: "SERIES",
          images: {
            img_1: "../../static/images/img_1.jpg",
            img_2: "../../static/images/img_1.jpg",
            img_3: "../../static/images/img_1.jpg"
          }
        },
        pelicula: {
          title: "PELICULAS",
          images: {
            img_1: "../../static/images/img_1.jpg",
            img_2: "../../static/images/img_1.jpg",
            img_3: "../../static/images/img_1.jpg"
          }
        }
      }
    };
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
    .DestacadoSection{
      margin-top: 10px;
    }
  }
}
</style>

<template>
    <div class="welcome-section">
        <div class="container">
            <div class="container__tittle"><h2 class="welcome-section__tittle">{{tittle}}</h2></div>   
            <div class="container__text"><p class="welcome-section__container">{{container}}</p></div>            
        </div>
    </div>
</template>

<script>
export default {
  name: "WelcomeSection",
  data() {
    return {
      tittle: "Bienvenidos a SWEETCRICTS",
      container:
        "Agrega críticas de música, juegos, televisión y películas de los principales críticos. Solo sweetcritic.com usa SWEETSCORES, lo que le permite saber de un vistazo cómo se revisó cada elemento."
    };
  }
};
</script>


<style lang="scss">
@import "../../src/assets/styles/1.settings/index";
.welcome-section {
  background: linear-gradient(to right, #0b72dc, #3ca6fd);
  color: white;
  height: 350px;
  display: flex;
  justify-content: center;
  align-items: center;
  .container {
    width: 60%;
    .container__tittle {
      display: flex;
      justify-content: center;
      .welcome-section__tittle {
        font-size: 32px;
        font-weight: 700;
        color: white;
      }
    }
    .container__text {
      display: flex;
      justify-content: center;
      .welcome-section__container {
        font-weight: 700;
        font-size: 22px;
        opacity: 0.6;
        line-height: 40px;
      }
    }
  }
}
</style>

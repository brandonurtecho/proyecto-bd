<template>
    <div class="info-section">
        <div class="info__tittle">
          <div class="title__container">
            <h1 class="tittle">Cualquier titulo aqui</h1>
          </div>
        </div>
        <div class="info__container">
            <div class="box__text" v-for="n in 5" :key="n">
              {{dato}}
            </div>               
        </div>
    </div>
</template>

<script>
export default {
  name: "InfoSection",
  data() {
    return {
      dato:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem quibusdam odio enim maiores voluptatibus magni consequuntur dolores ad repellat obcaecati vel quae minus, dolorem distinctio maxime ab reprehenderit voluptatem dolorum."
    };
  }
};
</script>

<style lang="scss">
@import "../../src/assets/styles/1.settings/index";
.info-section {
  height: 500px;
  background: $color-font-secondary;
  .info__tittle {
    display: flex;
    justify-content: center;
    .title__container {
      color: white;
      padding: 30px;
      .tittle {
        font-weight: 700;
      }
    }
  }
  .info__container {
    width: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    .box__text {
      // border-radius: 3px;
      width: 250px;
      height: 60%;
      background-color: #ffffff;
      box-shadow: 0px 7px 20px 0px rgba(0, 0, 0, 0.2);
      // margin: 0% 2% 0% 0%;
      padding: 2% 2% 2% 2%;
    }
  }
}
</style>

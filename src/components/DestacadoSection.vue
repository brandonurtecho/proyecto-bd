<template>
    <div class="destacado">
        <div class="destacado__title">
            <p class="title">
                {{destacadoData.title}}
            </p>
        </div>
        <div class="destacado__img">
            <div class="img__container" v-for="(item, index) in destacadoData.images" :key="index">
                <img class="img" :src="item" alt="" width="100%">
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: "DestacadoSection",
  props: ["destacadoData"],
  data() {
    return {};
  },
  created: function() {
    console.log(this.destacadoData.images);
  }
};
</script>

<style lang="scss">
@import "../../src/assets/styles/1.settings/index";
.destacado {
  .destacado__title {
    padding-top: 10px;
    display: flex;
    justify-content: center;
    .title {
      font-weight: 800;
      font-size: 40px;
    }
  }
  .destacado__img {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    .img__container {
      margin-top: 10px;
      background: #2f353a;
      width: 30%;
      .img {
        opacity: 0.65;
        cursor: pointer;
        transition: 0.3s;        
        &:hover {
          opacity: 1;
          transition: 0.3s;
        }
      }
    }
  }
}
</style>

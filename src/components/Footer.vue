<template>
    <div class="footer">
        <div class="container__text">
            <p class="text">BASE DE DATOS FISI</p>
        </div>        
    </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {};
  }
};
</script>

<style lang="scss">
@import "../../src/assets/styles/1.settings/index";
.footer {
  display: flex;
  justify-content: center;
  .container__text {
    padding-top: 50px;
    padding-bottom: 50px;
    opacity: 0.8;
    font-weight: 600;
    .text {
    }
  }
}
</style>

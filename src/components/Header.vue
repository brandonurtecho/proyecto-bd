<template>
    <div class="header">
        <a href="#default" class="header__logo">SWEETCRITICS</a>
        <div class="header__menu">
            <div class="container__item" >
              <a class="header__menu__item--active" href="#home">INICIO</a>
              <div class="container__dropdown">
                Brandon
              </div>
            </div>
            <div class="container__item">
              <a class="header__menu__item" href="#peliculas">PELICULAS</a>
              <div class="container__dropdown">
                BRANDON
              </div>
            </div>
            <div class="container__item" >
              <a class="header__menu__item" href="#juegos">JUEGOS</a>
              <div class="container__dropdown">
                BRANDON
              </div>
            </div>
            <div class="container__item" >
              <a class="header__menu__item" href="#tv">TV</a>
              <div class="container__dropdown">
                BRANDON
              </div>
            </div>
            <div class="container__item" >
              <a class="header__menu__item" href="#musica">MUSICA</a>
              <div class="container__dropdown">
                BRANDON
              </div>
            </div> 
            <div class="container__item" >
              <a class="header__menu__item" href="#musica">ANIME</a>
              <div class="container__dropdown">
                BRANDON
              </div>
            </div>                        
        </div>
    </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {};
  }
};
</script>

<style lang="scss">
@import "../../src/assets/styles/1.settings/index";
.header {
  display: flex;
  justify-content: space-between;
  padding: 15px 30px;
  // box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
  .header__logo {
    color: $color-font-primary;
    font-size: 23px;
    font-weight: 600;
    text-decoration: none;
  }
  .header__menu {
    display: flex;
    justify-content: space-around;
    .container__item {
      .container__dropdown {
        display: none;
        position: absolute;
        background-color: #f9f9f9;
        font-weight: 500;
        font-size: 12px;
        cursor: pointer;
        width: 160px;
        box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
        // border: solid 1px $color-font-primary;
        padding: 12px 16px;
        z-index: 10;
      }
      &:hover {
        .container__dropdown {
          display: flex;
        }
      }
      .header__menu__item {
        color: $color-font-primary;
        margin: 0px 10px;
        font-size: 20px;
        font-weight: 600;
        text-decoration: none;
        transition-duration: 0.5s;
        position: relative;

        &:hover {
          color: $color-font-secondary;
          transition-duration: 0.5s;
        }
        &::before {
          content: "";
          position: absolute;
          width: 0%;
          height: 5px;
          background: $color-font-secondary;
        }
        &:hover::before {
          content: "";
          position: absolute;
          width: 100%;
          top: -15px;
          height: 5px;
          background: $color-font-secondary;
          transition: all ease-in-out 0.15s;
        }
      }
      .header__menu__item--active {
        @extend .header__menu__item;
        color: $color-font-secondary;
      }
    }
  }
}
</style>

<template>
    <div class="header">
        <a href="#default" class="header__logo">SWEETCRITICS</a>
        <div class="header__nav">
            <div v-for="(navItem,index) in navItems" :key="index" class="nav__item" >
              <a :class="navItem.active?'item__name--active':'item__name'"  :href="navItem.link" @click="methodClick(index)">{{navItem.name}}</a>        
            </div>                              
        </div>
    </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      navItems: [
        {
          link: "#inicio",
          name: "INICIO",
          active: false
        },
        {
          link: "#peliculas",
          name: "PELICULAS",
          active: false
        },
        {
          link: "#juegos",
          name: "JUEGOS",
          active: false
        },
        {
          link: "#tv",
          name: "TV",
          active: false
        },
        {
          link: "#musica",
          name: "MUSICA",
          active: false
        },
        {
          link: "#anime",
          name: "ANIME",
          active: false
        },
        {
          link: "#about",
          name: "ABOUT",
          active: false
        }
      ]
    };
  },
  methods: {
    methodClick: function(itemIndex) {
      for (const item of this.navItems) item.active = false;
      this.navItems[itemIndex].active = true;
    }
  }
};
</script>

<style lang="scss">
@import "../../src/assets/styles/1.settings/index";
@import "../assets/styles/2.tools/index";
.header {
  display: flex;
  justify-content: space-between;
  padding: 20px 10px;
  color: $color-font-secondary;
  padding-bottom: 15px;
  // box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
  .header__logo {
    color: $color-font-primary;
    font-size: 23px;
    font-weight: 600;
    text-decoration: none;
  }
  .header__nav {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    .nav__item {
      &:hover {
        .dropdown {
          display: flex;
          .dropdown__item {
            display: flex;
            justify-content: center;
            list-style: none;
          }
        }
      }
      .item__name {
        color: $color-font-primary;
        margin: 0px 15px;
        font-size: 20px;
        font-weight: 600;
        text-decoration: none;
        transition-duration: 0.2s;
        position: relative;

        &:hover {
          color: $color-font-secondary;
          transition-duration: 0.2s;
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
          top: -20px;
          height: 5px;
          background: $color-font-secondary;
          transition: all ease-in-out 0.15s;
        }
      }
      .item__name--active {
        @extend .item__name;
        color: $color-font-secondary;
      }
    }
  }
  @include media-custom(925px) {
    .header__logo {
      display: none;
    }
    .header__nav {
      .nav__item {
        flex-basis: 100%;
        .item__name {
          justify-content: center;
        }
      }
    }
  }
}
</style>

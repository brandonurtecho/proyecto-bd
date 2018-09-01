<template>
    <div class="header">
        <a href="#default" class="header__logo">SWEETCRITICS</a>
        <div class="header__nav">
            <div v-for="(navItem,index) in navItems" :key="index" class="nav__item" >
              <a :class="navItem.active?'item__name--active':'item__name'"  :href="navItem.link" @click="methodClick(index)">{{navItem.name}}</a>
              <div class="dropdown">
                <ul v-for="dropdownItem in navItem.dropdownItems" :key="dropdownItem.index" class="dropdown__item">
                  <li>{{dropdownItem}}</li>                  
                </ul>
              </div>              
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
          active: false,
          dropdownItems: [
            "PC",
            "PS4",
            "Xbox One",
            "Switch",
            "Wii U",
            "3DS",
            "Vita",
            "IOS"
          ]
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
.header {
  display: flex;
  justify-content: space-between;
  padding: 15px 0px;
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
    .nav__item {
      .dropdown {
        color: $color-font-primary;
        font-family: "arial";
        display: none;
        position: absolute;
        background-color: #f9f9f9;
        font-weight: 500;
        font-size: 0.9em;
        cursor: pointer;
        width: 150px;
        box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
        // border: solid 1px $color-font-primary;
        padding: 12px 16px;
        z-index: 10;
      }
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
      .item__name--active {
        @extend .item__name;
        color: $color-font-secondary;
      }
    }
  }
}
</style>

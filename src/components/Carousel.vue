<template>
    <agile :infinite="true">
        <div class="slide slide--1"><h3>slide 1</h3></div>
        <div class="slide slide--2"><h3>slide 2</h3></div>
        <div class="slide slide--3"><h3>slide 3</h3></div>
        <div class="slide slide--4"><h3>slide 4</h3></div>
        <div class="slide slide--5"><h3>slide 5</h3></div>
        <div class="slide slide--6"><h3>slide 6</h3></div>
    </agile>
</template>

<script>
import Agile from "../../src/Agile";

export default {
  name: "Carousel",
  components: { Agile },
  data() {
    return {
    };
  }
};
</script>


<style lang="scss" type="text/scss">
@import "../../src/assets/scss/main.scss";
.agile {
  &__dots {
    bottom: 0;
    left: 50%;
    position: absolute;
    transform: translateX(-50%);
  }
  &__dot {
    button {
      background-color: transparent;
      border: 1px solid #fff;

      &:hover {
        background-color: #fff;
      }
    }

    &--current {
      button {
        background-color: #fff;
      }
    }
  }

  &__arrow {
    height: 100%;
    top: 0;
    width: 80px;

    &:hover {
      background-color: rgba(#000, 0.5);

      svg {
        fill: #fff;
      }
    }

    &[disabled] {
      display: none;
    }

    svg {
      fill: rgba(#fff, 0.4);
      height: 25px;
    }
  }
}

.slide {
  background: {
    position: center;
    size: cover;
  }
  height: 600px;

  &:before {
    background-color: rgba(#000, 0.2);
    content: "";
    height: 100%;
    left: 0;
    position: absolute;
    top: 0;
    width: 100%;
  }

  &--1 {
    background-image: url(..\assets\images\bg-01.jpg);
  }
  &--2 {
    background-image: url(..\assets\images\bg-02.jpg);
  }
  &--3 {
    background-image: url(..\assets\images\bg-03.jpg);
  }
  &--4 {
    background-image: url(..\assets\images\bg-04.jpg);
  }
  &--5 {
    background-image: url(..\assets\images\bg-05.jpg);
  }
  &--6 {
    background-image: url(..\assets\images\bg-06.jpg);
  }
}
</style>

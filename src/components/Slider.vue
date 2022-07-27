<template>
  <Carousel :items-to-show="2.5" :wrap-around="true">
    <Slide v-for="slide in 10" :key="slide">
      <div class="carousel__item">{{ slide }}</div>
    </Slide>
  </Carousel>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "MyCarousel",
  components: {
    Carousel,
    Slide,
  },
});
</script>

<style lang="scss" scoped>
.carousel {
  width: 100%;
  text-align: center;
  z-index: 1;

  &__item {
    min-height: 200px;
    width: 100%;
    background-color: rgb(0, 183, 255);
    color: white;
    font-size: 20px;
    border-radius: 8px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  &__slide {
    padding: 10px;
  }

  &__prev,
  &__next {
    box-sizing: content-box;
    border: 5px solid white;
  }
}
</style>

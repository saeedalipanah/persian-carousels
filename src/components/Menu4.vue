<template>
  <div class="menu-4 my-16" id="menu-4">
    <div
      class="background grid grid-cols-11"
      id="background-pic"
      :style="`background-image: url('/images/${slides[visibleSlide]}')`"
    >
      <div class="title col-span-11 mx-auto my-16 flex items-center">
        <div>منوی شماره 4</div>
      </div>
      <div class="col-start-4 col-span-5">
        <carousel
          @next="next"
          @prev="prev"
          :slides="slides"
          :visibleSlide="visibleSlide"
        >
          <carousel-slide
            v-for="(slide, index) in slides"
            :key="index"
            :visibleSlide="visibleSlide"
            :index="index"
          >
            <img class="image" :src="require(`@/assets/images/${slide}`)" />
          </carousel-slide>
        </carousel>
      </div>
    </div>
  </div>
</template>

<script>
import Carousel from "./carousels/menu4-carousel/Carousel.vue";
import CarouselSlide from "./carousels/menu4-carousel/CarouselSlide.vue";
export default {
  components: {
    Carousel,
    CarouselSlide,
  },
  data() {
    return {
      slides: [
        "slide(1).jpg",
        "slide(2).jpg",
        "slide(3).jpg",
        "slide(4).jpg",
        "slide(5).jpg",
        "slide(6).jpg",
        "slide(7).jpg",
        "slide(8).jpg",
        "slide(9).jpg",
      ],
      visibleSlide: 0,
    };
  },
  methods: {
    next() {

      if (this.visibleSlide >= this.slides.length - 1) {
        this.visibleSlide = 0;
      } else {
        this.visibleSlide++;
      }
    },
    prev() {

      if (this.visibleSlide <= 0) {
        this.visibleSlide = this.slides.length - 1;
      } else {
        this.visibleSlide--;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.menu-4 {
  .title {
    font-size: 1.875rem;
    color: white;
    font-weight: bold;
  }
  .image {
    width: 100%;
    height: 25rem;
    border-radius: 1.875rem;
    object-fit: cover;
  }
  .background {
    transition: all 1s ease;
    // background-image: url("../assets/images/slide(1).jpg");
    background-position: center;
    background-size: cover;
  }
}
</style>

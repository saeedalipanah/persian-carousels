<template>
  <div class="menu-4 my-16" id="menu-4">
    <div class="background grid grid-cols-11" id="background-pic">
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
              <img class="image" :src="slide"/>
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
        "https://i.picsum.photos/id/1021/2048/1206.jpg?hmac=fqT2NWHx783Pily1V_39ug_GFH1A4GlbmOMu8NWB3Ts",
        "https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY",
        "https://i.picsum.photos/id/1/5616/3744.jpg?hmac=kKHwwU8s46oNettHKwJ24qOlIAsWN9d2TtsXDoCWWsQ",
        "https://i.picsum.photos/id/1015/6000/4000.jpg?hmac=aHjb0fRa1t14DTIEBcoC12c5rAXOSwnVlaA5ujxPQ0I",
        "https://i.picsum.photos/id/1018/3914/2935.jpg?hmac=3N43cQcvTE8NItexePvXvYBrAoGbRssNMpuvuWlwMKg",
        "https://i.picsum.photos/id/227/1024/683.jpg?hmac=63Bm3-6abEba_BO4lpAKdrnmSL04wZpwK17xue1mCXw",
        "https://i.picsum.photos/id/1019/5472/3648.jpg?hmac=2mFzeV1mPbDvR0WmuOWSiW61mf9DDEVPDL0RVvg1HPs",
        "https://i.picsum.photos/id/1006/3000/2000.jpg?hmac=x83pQQ7LW1UTo8HxBcIWuRIVeN_uCg0cG6keXvNvM8g",
        "https://i.picsum.photos/id/152/3888/2592.jpg?hmac=M1xv1MzO9xjf5-tz1hGR9bQpNt973ANkqfEVDW0-WYU",
      ],
      visibleSlide: 0,
    };
  },
  methods: {
    next() {
      let backPic = document.getElementById("background-pic");

      if (this.visibleSlide >= this.slides.length - 1) {
        this.visibleSlide = 0;
      } else {
        this.visibleSlide++;
      }
      backPic.style.backgroundImage = `url(${this.slides[this.visibleSlide]})`;
    },
    prev() {
      let backPic = document.getElementById("background-pic");

      if (this.visibleSlide <= 0) {
        this.visibleSlide = this.slides.length - 1;
      } else {
        this.visibleSlide--;
      }
      backPic.style.backgroundImage = `url(${this.slides[this.visibleSlide]})`;
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
    background-image: url("https://i.picsum.photos/id/1021/2048/1206.jpg?hmac=fqT2NWHx783Pily1V_39ug_GFH1A4GlbmOMu8NWB3Ts");
    background-position: center;
    background-size: cover;
  }
}
</style>

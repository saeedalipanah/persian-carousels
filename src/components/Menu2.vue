<template>
  <div class="menu-2 flex flex-col items-center justify-center" id="menu-2">
    <div class="top-circle"></div>
    <Lines class="absolute top-40 mt-20 right-0"></Lines>
    <Lines class="absolute top-40 mt-20 -left-1"></Lines>

    <div class="title mb-10">منوی شماره 2</div>
    <menu-2-carousel 
      :slides="slides"
      :current="current"
      :prev="prev"
      :next="next"
    >
    </menu-2-carousel>
    
    <div class="controls flex justify-between -mb-8 w-full px-16">
      <div class="">
        <i @click="prevSlide" class="flex bi bi-chevron-right"></i>
      </div>
      <div class="points flex items-center mx-8" id="points">
        <div class="point" :class="`${i===current? 'active' : ''}`" v-for="(slide,i) in slides" :key="i"></div>
      </div>
      <div class="">
        <i @click="nextSlide" class="flex bi bi-chevron-left"></i>
      </div>
    </div>

    <div class="down-circle"></div>
  </div>
</template>

<script>
import Lines from "./shapes/Lines.vue";
import Menu2Carousel from "./carousels/menu2-carousel/Menu2Carousel.vue";

export default {
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
      current: 1,
      prev: 0,
      next: 2
    };
  },
  components: {
    Lines,
    Menu2Carousel,
  },
  methods: {
    nextSlide() {
      if(this.current === this.slides.length - 1) {
        this.current = 0;
        this.prev = this.slides.length - 1;
        this.next = 1;
      } else if(this.current === this.slides.length - 2) {
        this.current = this.slides.length - 1;
        this.prev = this.slides.length - 2;
        this.next = 0;
      } else if(this.current === 0) {
        this.prev = 0;
        this.next++;
        this.current++;
      } else {
        this.next++;
        this.prev++;
        this.current++;
      }
    },
    prevSlide() {
      if(this.current === 0) {
        this.current = this.slides.length - 1;
        this.prev = this.slides.length - 2;
        this.next = 0;
      } else if(this.current === 1) {
        this.current = 0;
        this.prev = this.slides.length - 1;
        this.next = 1;
      } else if (this.current === this.slides.length - 1) {
        this.next = this.slides.length - 1;
        this.current--;
        this.prev--;
      } else {
        this.next--;
        this.prev--;
        this.current--;
      }
    }
  }
};
</script>
<style lang="scss" scoped>
.menu-2 {
  overflow: hidden;
  position: relative;
  background: #019cd5;
  width: 100%;
  height: 65rem;
  .title{
    color:white;
    font-size: 1.875rem;
    font-weight: bold;
  }
  .top-circle {
    position: absolute;
    top: -15.9rem;
    right: -15%;
    width: 130%;
    height: 30rem;
    border-radius: 50%;
    background-color: white;
  }
  .down-circle {
    position: absolute;
    bottom: -15.9rem;
    right: -15%;
    width: 130%;
    height: 30rem;
    border-radius: 50%;
    background-color: white;
  }

  .controls {
  .bi {
      $color: white;
      $h-color: #777777;
      padding: .35rem;
    font-size: 1rem;
    color: $color;
    border: .125rem solid $color;
    border-radius: .625rem;
    cursor: pointer;
    transition: all .3s ease;
     &:hover{
         color : $h-color;
         border-color: $h-color ;
     }
    
  }
  .points {
    .point {
      height: .625rem;
      width: 10px;
      border-radius: 50%;
      background-color: rgb(173, 173, 173);
      margin: 0 3px;
      transition: all 0.5s ease;
      &.active {
        width: 25px;
        border-radius: 10px;
        background-color: rgb(255, 255, 255);
        transition: all 0.5s ease;
      }
    }
  }
  }
}
</style>

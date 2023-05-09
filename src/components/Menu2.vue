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
      width: .625rem;
      border-radius: 50%;
      background-color: rgb(173, 173, 173);
      margin: 0 .1875rem;
      transition: all 0.5s ease;
      &.active {
        width: 1.5625rem;
        border-radius: .625rem;
        background-color: rgb(255, 255, 255);
        transition: all 0.5s ease;
      }
    }
  }
  }
}
</style>

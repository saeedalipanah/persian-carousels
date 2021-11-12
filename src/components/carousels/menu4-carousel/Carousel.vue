<template>
  <div class="carousel">
    <slot></slot>
    <div class="flex justify-center pb-10 pt-12">
      <div class="">
        <i @click="prev" class="flex bi bi-chevron-right"></i>
      </div>
      <div class="points flex items-center mx-8" id="points">
        <div class="point" :class="`${i===visibleSlide? 'active' : ''}`" v-for="(slide,i) in slides" :key="i"></div>
      </div>
      <div class="">
        <i @click="next" class="flex bi bi-chevron-left"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["slides", "visibleSlide"],
  methods: {
    next() {
      this.$emit("next");
      
    },
    prev() {
      this.$emit("prev");

    },
    
  },
  
  
};
</script>

<style lang="scss">
.carousel {
  .bi {
      $color: white;
      $h-color: #777777;
      padding: .35rem;
    font-size: 1rem;
    color: $color;
    border: 2px solid $color;
    border-radius: 10px;
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
</style>

<template>
  <div class="slides-wrapper">
    <div class="slide" v-for="(slide, index) in slides" :key="index">
      <transition name="slide">
        <div class="s" v-if="index === activeSlide">
          <div class="fitst-service">{{ slide.beforeText }}</div>
          <div class="titr my-3">{{ slide.title }}</div>
          <div class="main-text">{{ slide.content }}</div>
        </div>
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  props: ["slides", "activeSlide"],
  methods: {},
};
</script>

<style lang="scss" scoped>
.slides-wrapper {
  position: relative;
  .slide {
    position: absolute;
  }
}
.fitst-service {
  font-weight: bold;
  font-size: 1.325rem;
  color: #2c2c30;
}
.titr {
  font-weight: 900;
  font-size: 3.375rem;
  font-weight: bold;
  color: #222222;
}
.main-text {
  text-align: justify;
  font-weight: normal;
  font-size: 1.05rem;
  line-height: 2.1rem;
  color: #2c2c30;
}
.slide-enter-active,
.slide-leave-active {
  transition: all 0.4s ease-in-out;
}

.slide-enter-from {
  opacity: 0;
  transform: translateX(100%);
}

.slide-leave-to {
  opacity: 0;
  transform: translateX(-100%);
}
.slide-leave-from,
.slide-enter-to {
  opacity: 1;
  transform: translateX(0px);
}
</style>

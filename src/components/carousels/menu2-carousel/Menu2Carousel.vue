<template>
  <div class="menu-crousel">
    <div class="carousel-items flex">
      <div
        class="carousel-item"
        v-for="(slide, i) in slides"
        :key="i"
        :class="`${
          i === current
            ? 'current'
            : i === prev
            ? 'prev'
            : i === next
            ? 'next'
            : ''
        }`"
      >
        <img :src="require(`@/assets/images/${slide}`)" alt="image" class="image" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["slides", "current", "next", "prev"],
  methods: {},
};
</script>

<style lang="scss" scoped>
.menu-crousel {
  height: 23rem;
  margin: 0 auto;
  width: 100%;
  overflow: hidden;
  position: relative;
  .carousel-items {
    height: 22rem;
    width: 100%;
    position: relative;
    .carousel-item {
      margin: 4rem auto 4rem;
      opacity: 0;
      padding: 1rem;
      position: absolute;
      top: 30%;
      left: 50%;
      transform: translate(calc(100% + 12rem), -50% scale(0.6));
      transition: all 1s ease;
      width: 30rem;
      height: 20rem;

      &.current {
        opacity: 1;
        transform: translate(-50%, -50%);
        z-index: 50;
        transition: all 1s ease;
      }
      &.prev {
        opacity: 0.5;
        transform: translate(30%, -50%) scale(0.8);
        transition: all 1s ease;
      }
      &.next {
        opacity: 0.5;
        transform: translate(-130%, -50%) scale(0.8);
        transition: all 1s ease;
      }
      .image {
        object-fit: cover;
        border: none;
        border-radius: 1.5rem;
        height: 100%;
        width: 100%;
        position: absolute;
        top: 0;
        box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5);
      }
    }
  }
}
</style>

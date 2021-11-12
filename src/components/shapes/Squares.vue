<template>
  <div class="wrapper flex ">
    <div class="squares ">
      <div
        class="square"
        v-for="(square,i) in squares"
        :key="i"
        :style="`width:${square.w};height:${square.h}; top: ${square.t};`"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      squares: [{ w: "6.25rem", h: "6.25rem",t:"2.5rem" },{ w: "8.75rem", h: "8.75rem" ,t:"1.25rem"},{ w: "11.25rem", h: "11.25rem",t:"0rem" }],
    };
  },
};
</script>

<style lang="scss" scoped>
.wrapper {
  overflow: hidden;

  .squares {
    width: 100%;
    height: 12.5rem;
    position: relative;
    margin: 3.125rem 0;

    .square {
      position: absolute;
      border: .0625rem solid #019cd5;
      transform: rotate(45deg);
      left: -5.625rem;
    }
  }
}
</style>

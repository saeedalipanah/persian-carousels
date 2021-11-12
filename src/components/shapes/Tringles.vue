<template>
  <div class="parent">
    <div class="triangle t-1" :style="'--t-color: ' + color"></div>
    <div class="triangle t-2" :style="'--t-color: ' + color"></div>
    <div class="triangle t-3" :style="'--t-color: ' + color"></div>
    <div class="triangle t-4" :style="'--t-color: ' + color"></div>
    <div class="triangle t-5" :style="'--t-color: ' + color"></div>
  </div>
</template>

<script>
export default {
    props: ['color']
};
</script>

<style lang="scss" scoped>
.parent {
  width: 100%;
  height: 31.25rem;
  position: absolute;
  overflow: hidden;

  .triangle {
    position: absolute;
    left: 0;
    width: 0;
    height: 0;
    border-top: 3.75rem solid var(--t-color);
    border-right: 2.1875rem solid transparent;
  }

  .t-1 {
    top: 0;
  }
  .t-2 {
    top: 80px;
  }
  .t-3 {
    top: 160px;
  }
  .t-4 {
    top: 240px;
  }
  .t-5 {
    top: 320px;
  }
}
</style>

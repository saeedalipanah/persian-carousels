<template>
  <div class="wrapper pt-0.5 pb-4">
    <div class="lines flex mt-6" v-for="i in 4" :key="i">
      <div
        class="line"
        v-for="deg in degs"
        :key="deg"
        :style="`transform: rotate(${deg})`"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      degs: ["-33deg", "33deg", "-33deg", "33deg", "-33deg", "33deg"],
    };
  },
};
</script>

<style lang="scss" scoped>
.wrapper {
    .lines {
        .line {
            margin-right: -0.5rem;
            width: 3.125rem;
            height: .0625rem;
            background: rgb(192, 192, 192);
        }
    }
}
</style>

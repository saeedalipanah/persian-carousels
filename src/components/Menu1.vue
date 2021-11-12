<template>
  <div class="menu-1 py-28 mt-24" id="menu-1">
    <div class="floating-icons flex flex-col">
      <span class="fab fa-twitter fa-2x"></span>
      <span class="fab fa-linkedin fa-2x"></span>
      <span class="insta-icon fab fa-instagram fa-2x"></span>
      <span class="fab fa-facebook fa-2x"></span>
    </div>
    <div class="first-wrapper grid grid-cols-11">
      <div class=" col-span-6 mr-40 overflow-hidden relative" >
        <text-carousel
          :slides="slides"
          :active-slide="activeSlide"
          class=""
        ></text-carousel>
        <div class="points flex justify-center absolute bottom-1 left-1/2
        " id="text-slider-points ">
          <div @click="changeSlide(i)" class="text-point mx-1 " :class="`${i===activeSlide ? 'active' : ''}`" v-for="(slide,i) in slides" :key="i" ></div>
        </div>
      </div>
      <div
        class="
          
          
           col-span-5
          flex
          justify-center
          justify-start
          mb-10
          
        "
      >
        <div class="square"></div>
      </div>
    </div>
  </div>
</template>
<script>
import TextCarousel from "./carousels/text-carousel/TextCarousel.vue";
export default {
  data() {
    return {
      slides: [
        {
          beforeText: "سرویس اول",
          title: "تیتر 1",
          content:
            " لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد. ",
        },
        {
          beforeText: "سرویس دوم",
          title: "تیتر 2",
          content:
            " لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد. ",
        },
        {
          beforeText: "سرویس سوم",
          title: "تیتر 3",
          content:
            " لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد. ",
        },
        {
          beforeText: "سرویس چهارم",
          title: "تیتر 4",
          content:
            " لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد. ",
        },
      ],
      activeSlide: 2,
    };
  },
  components: {
    TextCarousel,
  },
  methods:{
    changeSlide(i){
      this.activeSlide = i
    }
  },

  created() {
    setInterval(() => {
      this.activeSlide++;
      if (this.activeSlide >= this.slides.length) this.activeSlide = 0;
    }, 3000);
  },
};
</script>
<style lang="scss" scoped>
.menu-1 {
  .floating-icons {
    position: fixed;
    right: 4rem;
    z-index: 50;
    * {
      color: #797877;
      margin: 1.2rem 0;
      transition: color 0.5s ease;
      &:hover {
        color: #019cd5;
        cursor: pointer;
      }
    }
  }
  .first-wrapper {
    .points {
      .text-point {
        height: .75rem;
        width: .75rem;
        border-radius: 50%;
        background-color: rgb(216, 216, 216);
        cursor: pointer;
        transition: all 0.2s ease;
        &.active {
          
          border-radius: 10px;
          background-color: #019cd5;
          transition: all 0.2s ease;
        }
        &:hover{
          transform: scale(1.3);
        }
      }
    }
  }
  .square {
    height: 17rem;
    width: 17rem;
    background: linear-gradient(
      316.88deg,
      #019cd5 19.45%,
      rgba(255, 255, 255, 0.5) 94.24%
    );
    border-radius: 4rem;
    transform: rotatez(45deg);
  }
}

</style>

<template>
  <Triangles class="left" :color="'#FD3D3943'"></Triangles>
  <Triangles class="right" :color="'#808080'"></Triangles>
  <navigation></navigation>

  <menu-1></menu-1>
  <second-section></second-section>
  <menu-2> </menu-2>
  <menu-3></menu-3>
  <menu-4 ></menu-4>
  
  <menu-5></menu-5>
  <Footer></Footer>
</template>

<script>
import Navigation from "./components/Navigation.vue";
import Menu1 from "./components/Menu1.vue";
import SecondSection from "./components/SecondSection.vue";
import Menu3 from "./components/Menu3.vue";
import Menu4 from "./components/Menu4.vue";
import Menu5 from "./components/Menu5.vue";
import Menu2 from "./components/Menu2.vue";
import Footer from "./components/Footer.vue";
import Triangles from "./components/shapes/Tringles.vue";



export default {
  name: "App",
  components: {
    Navigation,
    Menu1,
    SecondSection,
    Menu2,
    Menu3,
    Menu4,
    Menu5,
    Footer,
    Triangles,
    
    
  },
  data() {
    return {
      
    };
  },
};
</script>

<style lang="scss">
@font-face {
  font-family: "vazir";
  src: url("./assets/fonts/Farsi-Digits/Vazir-FD.eot");
  src: url("./assets/fonts/Farsi-Digits/Vazir-FD.eot?#iefix")
      format("Vazir-FD-opentype"),
    url("./assets/fonts/Farsi-Digits/Vazir-FD.woff") format("woff"),
    url("./assets/fonts/Farsi-Digits/Vazir-FD.ttf") format("truetype");
  font-weight: normal;
  font-style: normal;
}
@font-face {
  font-family: "vazir";
  src: url("./assets/fonts/Farsi-Digits/Vazir-Bold-FD.eot");
  src: url("./assets/fonts/Farsi-Digits/Vazir-Bold-FD.eot?#iefix")
      format("Vazir-FD-opentype"),
    url("./assets/fonts/Farsi-Digits/Vazir-Bold-FD.woff") format("woff"),
    url("./assets/fonts/Farsi-Digits/Vazir-Bold-FD.ttf") format("truetype");
  font-weight: 900;
  font-style: bold;
}
@font-face {
  font-family: "vazir";
  src: url("./assets/fonts/Farsi-Digits/Vazir-Light-FD.eot");
  src: url("./assets/fonts/Farsi-Digits/Vazir-Light-FD.eot?#iefix")
      format("Vazir-FD-opentype"),
    url("./assets/fonts/Farsi-Digits/Vazir-Light-FD.woff") format("woff"),
    url("./assets/fonts/Farsi-Digits/Vazir-Light-FD.ttf") format("truetype");
  font-weight: 300;
  font-style: normal;
}
html {
  scroll-behavior: smooth;
  scroll-padding-top: 7.1875rem;
}
* {
  font-family: "vazir";
  direction: rtl;
  margin: 0;
  padding: 0;
}
:root {
  font-size: 4px;
  @media only screen and (min-width: 450px) {
    font-size: 6px;
  }
  @media only screen and (min-width: 640px) {
    font-size: 9px;
  }
  @media only screen and (min-width: 768px) {
    font-size: 10px;
  }
  @media only screen and (min-width: 900px) {
    font-size: 12px;
  }
  @media only screen and (min-width: 1024px) {
    font-size: 13px;
  }
  @media only screen and (min-width: 1280px) {
    font-size: 17px;
  }
  @media only screen and (min-width: 1536px) {
    font-size: 20px;
  }
}

.left {
  top: 34.375rem;
  z-index: -10;
}
.right {
  max-width: 100px;
  top: 193.75rem;
  transform: rotateY(180deg);
}


</style>

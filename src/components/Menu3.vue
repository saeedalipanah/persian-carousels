<template>
  <div class="menu3 grid grid-cols-2 gap-10 justify-around  mx-auto w-10/12  md:w-11/12 py-20" id="menu-3">
    <div class="col-span-2  lg:col-span-1 pr-10 ">
      <div class="title text-4xl font-bold ">منوی شماره 3</div>
      <div class="main-text my-5 text-center  ">
        لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده
        از طراحان گرافیک است.
      </div>
      <button class="px-10 py-2">بیشتر بدانیم</button>
    </div>
    <div class="col-span-2 lg:col-span-1  ">
      <img
        class="m-auto"
        src="https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80"
      />
    </div>
    <Squares class="right-square"></Squares>
  </div>
</template>
<script>
import Squares from './shapes/Squares.vue'
export default {
  components:{
    Squares
  }
}
</script>
<style lang="scss" scoped>
.menu3 {
  position: relative;
  .title {
    color: #222222;
  }
  .main-text {
    font-size: 1.125rem;
    line-height: 3.125rem;
    text-align: right;
  }
  button{
   border: .0625rem solid #797877;;
   border-radius: .625rem;
   color: #797877;
  }
  img {
    width: 40.625rem;
    height: 25rem;
    border-radius: 1.875rem;
  }
  .right-square{
    position: absolute;
    transform: rotateY(180deg);
    width: 18.75rem;
    right: -3.75rem;
    bottom: -4.6875rem;
  }
}
</style>

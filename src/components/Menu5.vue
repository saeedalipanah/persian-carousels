<template>

    
  <div class=" my-16  relative" id="menu-5">
    
    <Squares class="sq"></Squares>
    <div class="menu5 w-10/12 md:w-7/12 mx-auto">
      <div class="menu-title text-center text-3xl font-black mb-16">
        منوی شماره 5
      </div>
      <div class="grid grid-cols-3 gap-10">
        <div class="col-span-3 lg:col-span-1">
          <div class="title my-1">نام و نام خانوادگی</div>
          <input
            class="py-3 w-full"
            type="text"
            name="name"
            id="name"
            placeholder="    نام و نام خانوادگی خود را وارد کنید"
          />
        </div>
        <div class="col-span-3 lg:col-span-1">
          <div class="title my-1">شماره تماس</div>
          <input
            class="py-3 w-full"
            type="text"
            name="name"
            id="name"
            placeholder="    شماره تماس خود را وارد کنید"
          />
        </div>
        <div class="col-span-3 lg:col-span-1">
          <div class="title my-1">ایمیل</div>
          <input
            class="py-3 w-full"
            type="text"
            name="name"
            id="name"
            placeholder="     آدرس ایمیل خود را وارد کنید"
          />
        </div>
      </div>
      <div class="grid grid-col-1 mt-4">
        <div class="title my-1">پیام</div>
        <input
          class="pt-2 pb-16 w-full"
          type="text"
          name="name"
          id="name"
          placeholder="     اینجا بنویسید..."
        />
      </div>
      <div class="flex justify-center md:justify-end">
        <button class="btn-cta  my-10">CTA</button>
      </div>
    </div>
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

  .sq{
    position: absolute;
    width: 18.75rem;
    left: 0;
    top: -217px;
  }
.menu5 {
  .menu-title {
    color: #222222;
  }
  .title {
    font-size: .8rem;
    color: #2c2c30;
  }
  input {
    border-radius: 0.625rem;
    border: .0625rem solid #b2b2b2;
    font-size: 0.7375rem;
  }
  .btn-cta {
    
    background: #019cd5;
    font-size: 0.76rem;
    border-radius: 1.875rem;
    border: none;
    color: white;
    padding: .525rem 4.625rem;
  
  }
}
</style>

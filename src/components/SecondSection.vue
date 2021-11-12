<template>
  <div class="second-sec grid grid-cols-3 gap-8 px-24 pt-20">
    <div class="box col-span-1 flex items-center ">
      <div class="first p-10  mx-auto">
        <div class="title">ویژگی دوم</div>
        <div class="main-text">
          لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده
          از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و
          سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای
          متنوع با هدف بهبود ابزارهای کاربردی می باشد.
        </div>
      </div>
    </div>
    <div class="col-span-1">
      <div class="between px-10 py-14  mx-auto my-10 ">
        <div class="title">ویژگی اول</div>
        <div class="main-text">
          لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده
          از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و
          سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای
          متنوع با هدف بهبود ابزارهای کاربردی می باشد.
        </div>
      </div>
    </div>
    <div class="col-span-1 flex items-center ">
      <div class="last p-10  mx-auto">
        <div class="title">ویژگی سوم</div>
        <div class="main-text">
          لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده
          از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و
          سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای
          متنوع با هدف بهبود ابزارهای کاربردی می باشد.
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.second-sec {
  .between {
    &:hover {
      transform: scale(1.1);
    }

    transition: all 0.5s ease;
    background: #fd3d39;
    box-shadow: 0rem 0.25rem 1rem rgba(34, 34, 34, 0.16);
    border-radius: 2.8125rem;
    .title {
      margin-bottom: 1.5625rem;
      font-style: normal;
      font-weight: bold;
      font-size: 2rem;
      
      text-align: center;
      color: #ffffff;
    }
    .main-text {
      font-style: normal;
      font-weight: normal;
      font-size: 0.8125rem;
      line-height: 1.8rem;
      text-align: right;
      color: #ffffff;
    }
  }
  .first {
    &:hover {
      transform: scale(1.1);
    }
    transition: all 0.5s ease;
    background: #16a8fc;
    box-shadow: 0rem 0.25rem 1rem rgba(34, 34, 34, 0.16);
    border-radius: 2.8125rem;
    .title {
      margin-bottom: 1.5625rem;
      font-style: normal;
      font-weight: bold;
      font-size: 2rem;
      
      text-align: center;
      color: #ffffff;
    }
    .main-text {
      font-style: normal;
      font-weight: normal;
      font-size: 0.8125rem;
      line-height: 1.8rem;
      text-align: right;
      color: #ffffff;
    }
  }
  .last {
    &:hover {
      transform: scale(1.1);
    }
    transition: all 0.5s ease;
    background: #16a8fc;
    box-shadow: 0rem 0.25rem 1rem rgba(34, 34, 34, 0.16);
    border-radius: 2.8125rem;
    .title {
      margin-bottom: 1.5625rem;
      font-style: normal;
      font-weight: bold;
      font-size: 2rem;
      text-align: center;
      color: #ffffff;
    }
    .main-text {
      font-style: normal;
      font-weight: normal;
      font-size: 0.8125rem;
      line-height: 1.8rem;
      text-align: right;
      color: #ffffff;
    }
  }
}
</style>

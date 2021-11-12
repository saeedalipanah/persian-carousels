<template>
  <div class="footer px-10 py-6" id="footer">
    <a class="return-button px-4 py-2.5" href="#menu-1" >
      بازگشت به بالا<i class="fas fa-chevron-up mx-2"></i>
    </a>
    <div class="grid grid-cols-12 gap-10 mr-10">
      <div class="col-span-3 flex flex-col items-center md:items-start">
        <div class="logo">LOGO</div>
        <div class="main-text">
          ورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده
          از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و
          سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای
          متنوع با هدف بهبود ابزارهای کاربردی می باشد. کتابهای زیادی در شصت و سه
          درصد گذشته،
        </div>
      </div>
      <div class="col-span-4 flex flex-col items-center py-6 mr-6">
        <div class="fast-access mb-4">دسترسی سریع</div>
        <a href="#menu-1" class="menu-number mb-2">منوی شماره 1</a>
        <a href="#menu-2" class="menu-number mb-2">منوی شماره 2</a>
        <a href="#menu-3" class="menu-number mb-2">منوی شماره 3</a>
        <a href="#menu-4" class="menu-number mb-2">منوی شماره 4</a>
        <a href="#menu-5" class="menu-number mb-2">منوی شماره 5</a>
      </div>
      <div class="col-span-5 flex flex-col items-start py-5 mr-10">
        <div class="contact-us ">تماس با ما</div>
        <div class="address flex items-center my-2">
          <span class="material-icons ml-2">place</span> تهران، پاسداران، خیابان
          نجفی، کوچه اقاقیا،پلاک 2 واحد 11
        </div>
        <div class="phone flex items-center my-1">
          <span class="material-icons ml-2">phone_in_talk</span> (+98)2222222222
        </div>
        <div class="fax flex items-center my-1">
          <span class="material-icons ml-2">print</span> (+98)2222222222
        </div>
        <div class="email flex items-center my-1">
          <span class="material-icons ml-2">email</span> Info@peak-elevator.com
        </div>
        <div class="icons flex items-center mt-2">
          <span class="fab fa-twitter fa-2x ml-5"></span>
          <span class="fab fa-linkedin fa-2x mx-5"></span>
          <span class="insta-icon fab fa-instagram fa-2x mx-5"></span>
          <span class="fab fa-facebook fa-2x mr-5"></span>
        </div>
      </div>
    </div>
  </div>
  <div class="container-last grid grid-col-1">
    <div class="last py-3 text-center">
      تمامی حقوق این وبسایت متعلق به سایت فلان می باشد
    </div>
  </div>
</template>
<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@700;900&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;700;900&display=swap");
* {
  color: #ffffff;
}
.footer {
  background-color: #2c2c30;
  position: relative;
  .return-button {
    position: absolute;
    top: 40px;
    left: 20px;
    font-size: 0.7rem;
    border: 0.0625rem solid #ffffff;
    border-radius: 0.625rem;
    color: #ffffff;
    cursor: pointer;
  }
  .logo {
    font-family: "Poppins", sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 2.5rem;
    line-height: 5rem;
  }
  .main-text {
    font-weight: 500;
    font-size: 0.7125rem;
    line-height: 1.675rem;
    text-align: justify;
  }
  .address {
    font-size: 0.6125rem;
  }
  .fax,
  .phone {
    font-family: "Poppins", sans-serif;
    font-weight: normal;
  }
  .email {
    font-family: "Poppins", sans-serif;
    font-size: 0.7375rem;
  }
  .icons {
    * {
      cursor: pointer;
      transition: color 0.2s ease-in;
      &:hover {
        color: #019cd5;
      }
    }
  }
  .fast-access {
    font-weight: bold;
    font-size: 1.2rem;
  }

  .menu-number {
    font-weight: 500;
    font-size: 0.8rem;

    cursor: pointer;
    transition: color 0.2s ease-in;
    &:hover {
      color: #019cd5;
    }
  }
  .contact-us {
    font-style: normal;
    font-weight: bold;
    font-size: 1.1rem;
  }
}
.container-last {
  background-color: #019cd5;
  .last {
    font-weight: 300;
    font-size: 0.7375rem;
  }
}
</style>

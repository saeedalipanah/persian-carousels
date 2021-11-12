<template>
  <div class="nav py-2" >
    <div class="grid grid-cols-5 gap-4">
      <div class="col-span-1 mx-auto   my-auto ">
        <button class="btn-cta">CTA</button>
      </div>
      <div class="col-span-3  my-auto">
        <ul class="flex justify-start mr-8">
          <li><a href="#menu-1">منوی شماره 1</a></li>
          <li><a href="#menu-2">منوی شماره 2</a></li>
          <li><a href="#menu-3">منوی شماره 3</a></li>
          <li><a href="#menu-4">منوی شماره 4 </a></li>
          <li><a href="#menu-5">منوی شماره 5 </a></li>
          <li><a href="#footer">فوتر</a> </li>
        </ul>
      </div>
      <div class="col-span-1  flex justify-center">
        <div class="logo">LOGO</div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@700;900&display=swap");
.nav {
  box-shadow: 0px 2px 8px rgba(34, 34, 34, 0.15);
  position: fixed;
  top: 0;
  width: 100%;
  background-color: white;
  z-index: 100;
  .btn-cta {
    background: #019cd5;
    font-size: 0.76rem;
    border-radius: 1.875rem;
    border: none;
    color: white;
    padding: .525rem 4.625rem;
  }

  ul {
    li {
      font-size: 1rem;
      margin-left: 1.7375rem;
      
      color: #797877;
      * {
      cursor: pointer;
      transition: color 0.2s ease-in;
      &:hover {
        color: #019cd5;
      }
    }
    }
  }
  .logo {
    font-family: "Poppins";
    font-style: normal;
    font-weight: bold;
    font-size: 2.7375rem;
    text-align: right;
  }
}
</style>

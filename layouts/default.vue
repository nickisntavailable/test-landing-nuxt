<template>
  <div class="container-menu">
    <div class="navbar-menu">
      <div class="menu-logo">
        <nuxt-link to="/" exact class="logo-wrapper">
          <div class="logo-icon"></div>
          <div class="logo-text">Моя Квартира</div>
        </nuxt-link>
        <!-- <a href="#" class="logo-wrapper">
          
        </a> -->
      </div>

      <div class="menu-items">
        <div class="menu-links">
          <nuxt-link to="/rooles" class="item">Правила</nuxt-link>
          <nuxt-link to="/instructions" class="item">Инструкция</nuxt-link>
          <nuxt-link to="/agreements" class="item">Соглашения</nuxt-link>
        </div>
        <button>Войти</button>
      </div>
    </div>
    <nuxt/>
  </div>
</template>

<style lang="scss">

a { 
  text-decoration: none;
}

.menu-logo .logo-wrapper {
  display: flex;
  align-items: center;

  .logo-icon {
    background-image: url(../assets/service-icon5.png);
    background-repeat: no-repeat;
    display: inline-block;
    background-size: 200px;
    background-position: -80px -240px;
    width: 40px;
    height: 40px;
    margin-left: -8px;
    margin-right: 10px;
  }

  .logo-text {
    
    font-weight: 700;
    font-size: 24px;
    color: #333;
    letter-spacing: -0.5px;
    margin-right: -10px;
  }
}


.navbar-menu {
  min-height: 80px;
  height: 80px;
  width: 100vw;
  display: flex;
  position: sticky;
  justify-content: space-between;
  align-items: center;
  padding: 0 32px;
  margin: 0;
  box-shadow: 0 1px 6px 0 rgba(0,0,0,.14);
  background: hsla(0,0%,100%,.98);


  .menu-items {
    display: flex;
    align-items: center;

    .menu-links {
      font-family: PT Sans, sans-serif;
      .item {
        font-size: 16px;
        color: rgb(100, 100, 100);
        margin-right: 32px;
        &:hover {
          color: rgb(168, 163, 163);
        }
      }

      
    }

    button {
      width: 140px;
      height: 44px;
      text-align: center;
      background-color: #fff;
      color: #000;
      border-color: rgb(26, 37, 139);
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 30px;
      font-size: 16px;
      outline: none;

      &:hover {
        color: #fff;
        background-color: rgb(26, 37, 139);
        
      }
    }

  }
}




</style>


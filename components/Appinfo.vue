<template>
  <section class="container-app">
    <div class="app-info">
      <div class="app-info-title">
        Приложение для решения текущих вопросов по дому онлайн
      </div>
      <div class="app-info-text">
        Поможет решить проблемы жителей дома в режиме реального времени, без дополнительных визитов и звонков в управляющую организацию
      </div>
      <div class="app-info-buttons">
        <a href="#" class="connect">Попробовать бесплатно</a>
        <a href="#">
          <img src="https://play.google.com/intl/en_us/badges/images/generic/ru_badge_web_generic.png" alt="Доступно в Google Play" class="google-play">
        </a>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  components: {
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}


.container-app {
  min-height: 502px;
  color: #333;
  padding: 95px 0;
  height: 502px;
  background: url(../assets/background.jpg) center center/cover no-repeat;
  z-index: -1;


  .app-info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    // width: 90%;
    margin: 0 95px;


    &-title {
      font-family: "PT Serif", serif;
      font-size: 34px;
      font-weight: 700;
      line-height: 43px;
      margin-bottom: 17px;
      width: 50%;
      margin-bottom: 20px;
    }

    &-text {
      font-size: 21px;
      line-height: 26px;
      width: 40%;
      font-family: "PT Sans", sans-serif;
      margin-bottom: 55px;
    }

    &-buttons {
      display: flex;
      align-items: center;

      .connect {
        min-width: 240px;
        height: 50px;
        margin: 0 10px 0 0;
      }
      
      .google-play {
        height: 76px;
      }
    }
  }
}

.connect {
        font-family: "PT Sans", sans-serif;
        text-transform: uppercase;
        font-weight: bold;
        font-size: 15px;
        text-align: center;
        text-decoration: none;
        line-height: 50px;
        display: block;
        padding: 0 28px;
        background-color: #e12351;
        -ms-border-radius: 4px;
        border-radius: 4px;
        color: #ffffff;
        cursor: pointer;
        border: none;
      }


</style>


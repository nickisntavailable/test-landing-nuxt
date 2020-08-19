<template>
  <footer>
      <div class="links">
          <div class="row">
              <div class="col">
                  <div class="lk">
                      <a href="">Личный кабинет</a>
                  </div>
                  <div class="question">
                      <a href="">Задать вопрос</a>
                  </div>
                  <div class="email-director">
                      <a href="">Письмо директору</a>
                  </div>
                  <div class="icon-circle">
                      <a href="">
                          <img src="../assets/site-map.png" alt="">
                      </a>
                  </div>
              </div>
              <div v-for="col in cols" :key="col.title" class="col">
                  <div class="col-title">
                      {{col.title}}
                  </div>
                  <ul v-for="ul in col.uls" :key="ul">
                      <li><a href="">{{ul}}</a></li>
                  </ul>
              </div>
              
          </div>
      </div>

      <div class="contacts">
          <div class="contacts-wrap">
              <div class="icons">
                  <div class="social">
                      <div class="vk">
                          <font-awesome-icon :icon="['fab', 'vk']" :style="{ color: 'white' }"/>
                      </div>
                      <div class="fb">
                          <font-awesome-icon :icon="['fab', 'facebook-f']" :style="{ color: 'white' }"/>
                      </div>
                      <div class="odn">
                          <font-awesome-icon :icon="['fab', 'odnoklassniki']" :style="{ color: 'white' }"/>
                      </div>
                      <div class="yt">
                          <font-awesome-icon :icon="['fab', 'youtube']" :style="{ color: 'white' }"/>
                      </div>
                      <div class="tw">
                          <font-awesome-icon :icon="['fab', 'twitter']" :style="{ color: 'white' }"/>
                      </div>
                      <div class="vb">
                          <font-awesome-icon :icon="['fab', 'viber']" :style="{ color: 'white' }"/>
                      </div>
                      <div class="tg">
                          <font-awesome-icon :icon="['fab', 'telegram-plane']" :style="{ color: 'white' }"/>
                      </div>
                  </div>
                  <div class="email">
                      <p>Наша почта:</p>
                      <a href="#">mail@roskvartal.ru</a>
                  </div>
              </div>
              <div class="phone">
                  <p>Бесплатный звонок<br>по всей территории России</p>
                  <p class="number">8 800 500-65-61</p>
                  <button class="order">Заказать звонок</button>
              </div>
          </div>
      </div>
  </footer>
</template>

<script>

export default {
  data() {
      return {
          cols: [
              {
                title: 'КОМПАНИЯ',
                uls: [
                    'О нас',
                    'Команда',
                    'Работа у нас',
                    'Часто задаваемые вопросы',
                    'Материалы для СМИ',
                    'Официальные документы',
                ]
              },
              {
                title: 'УСЛУГИ',
                uls: [
                    'ГИС ЖКХ',
                    'Реформа ЖКХ',
                    'Снижение ОДН',
                    'Проведение ОСС',
                    'Сайт для УК/ТСЖ',
                    'Юридическая поддержка',
                ]
              },
              {
                title: 'ПОЛЕЗНЫЕ СЕРВИСЫ',
                uls: [
                    'Портал',
                    'Сервис «ОСС на 100%»',
                    'Сообщество «Про ЖКХ»',
                    'Онлайн-школа ЖКХ',
                    'Лицензионный тест УК',
                    'Новый вебинар для УК/ТСЖ'
                ]
              },
          ]
      };
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}




footer {

    .links {
        min-height: 270px;
        background-color: #006bb7;
        padding: 40px 0 35px 0;
        display: flex;
        justify-content: center;
        align-items: center;
        .row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1134px;
            width: 100%;

            .col {
                
                font-family: "PT Sans", sans-serif;

                a {
                    text-decoration: none;
                    cursor: pointer;
                }
                &-title {
                    font-size: 16px;
                    font-weight: 700;
                    color: #fff;
                    margin-bottom: 25px;
                    text-transform: uppercase;
                }
                ul {
                    list-style: none;
                    padding: 0;
                    margin: 0;
                    li {
                        margin-bottom: 5px;
                        a {
                            font-size: 16px;
                            color: #ccc;
                            &:hover {
                                color: #fff;
                            }
                        }
                    }
                }
                .lk {
                    font-weight: 100;
                    font-size: 22px;
                    position: relative;
                    left: -20px;
                    a {
                        padding: 10px 20px;
                        border: 1px solid #fff;
                        border-radius: 30px;
                        color: #ccc;
                        &:hover {
                            color: #fff;
                        }
                    }
                }
                .question, .email-director {
                    margin-top: 30px;
                    
                    font-size: 20px;
                    padding: 0;
                    width: 100%;
                    display: block;
                    a {
                        color: #ccc;
                        &:hover {
                            color: #fff;
                        }
                    }
                }
                .email-director {
                    font-size: 16px;
                }
                .icon-circle {
                    margin-top: 20px;
                    margin-left: -10px;
                    margin-right: 15px;
                    width: 32px;
                    height: 32px;
                    text-align: center;
                    vertical-align: middle;
                    line-height: 36px;
                    border-radius: 100%;
                    background-color: transparent;
                    &:hover {
                        background-color: rgba(0,0,0,.5);
                    }
                }
            }
        }
    }

    .contacts {
        background-color: #2a3c4e;
        padding: 20px 0;
        min-height: 82px;
        display: flex;
        align-items: center;
        justify-content: center;
        &-wrap {
            font-family: PT Sans, sans-serif;
            display: flex;
            align-items: center;
            justify-content: space-between;
            font-size: 14px;
            color: #979797;
            max-width: 1170px;

            .icons, .phone {
                display: flex;
                align-items: center;
                justify-content: space-between;
            }
        }

        .social {
            display: flex;
            align-items: center;

            .vk, .fb, .odn, .yt, .tw, .vb, .tg {
                width: 32px;
                height: 32px;
                border-radius: 50%;
                text-align: center;
                margin-right: 20px;
                padding-top: 6px;
            }

            .vk {
                background-color: rgb(11, 15, 230);
            }
            .fb {
                background-color: rgb(11, 15, 230);
            }
            .odn {
                background-color: rgb(230, 135, 11);
            }
            .yt {
                background-color: rgb(230, 11, 11);
            }
            .tw {
                background-color: rgb(11, 150, 230);
                padding-top: 8px;
            }
            .vb {
                background-color: rgb(150, 11, 230);
                padding-top: 8px;
            }
            .tg {
                background-color: rgb(11, 150, 230);
                padding-top: 8px;
            }
        }


        .email {
            margin-left: 57px;
            p {
                font-size: 14px;
                color: #979797;
                margin: 0;
            }
            a {
                color: #fff;
                text-decoration: underline;
            }
        }

        .phone {
            p {
                text-align: right;
                margin-left: 20px;
            }
            .number {
                font-size: 32px;
                color: #fff;
                margin-left: 15px;
            }
            .order {
                padding: 10px 20px;
                border-radius: 4px;
                background-color: #007be5;
                text-align: center;
                font-size: 14px;
                color: #fff;
                font-weight: 700;
                border: none;
                margin-left: 30px;
                outline: none;
            }
        }
    }
}


</style>


<template>
  <section class="usage">
    <div class="container">
        <div class="main-title">
            кто может пользоваться
        </div>
        <div class="users">
            <div class="users-img"></div>
            <div class="users-bar"></div>
        </div>
        <div class="cons">
            <img class="cons-img" src="../assets/img_mnogokvartir.svg" alt="">
    
            <div class="cons-text-container">
                <div class="cons-title">
                    Жители многоквартирных домов
                </div>
                <ul v-for="list in lists" :key="list">
                    <li>{{list}}</li>
                </ul>
                <a href="#" class="connect">Зарегистрировать личный кабинет</a>
            </div>
        </div>
        <div class="cons">
            <div class="cons-text-container">
                <div class="cons-title">
                    Управляющие организации и ТСЖ
                </div>
                <ul v-for="uc_tsg in uc_tsgs" :key="uc_tsg">
                    <li>{{uc_tsg}}</li>
                </ul>
                <a href="#" class="connect">Зарегистрировать личный кабинет</a>
            </div>
            <img class="uc-tsg" src="../assets/img_upr_company.svg" alt="">
        </div>
    </div>
  </section>
</template>

<script>

export default {
  data() {
      return {
          lists: [
              'Получение сведений о квартире, доме, лицевом счёте и управляющей организации',
              'Отправка обращений или вопроса в управляющую организацию, ТСЖ или ЖСК',
              'Передача показаний счётчиков',
              'Вызов аварийной службы',
              'Запись на приём к руководителю управляющей организации',
              'Новости дома и района',
              'Публикация объявлений для жителей вашего дома',
              'Отправка заявок на устранение проблемы и оценка качества её выполнения',
              'Организация совместных мероприятий с управляющей организацией',
          ], 
          uc_tsgs: [
              'Быстрое и надёжное информирование жителей МКД',
              'Работа с обращениями',
              'Возможность прикрепления фото- и видеоматериалов',
              'Получение заявок на выполнение работ',
              'Обратная связь от жителей МКД',
              'Контроль потребления коммуналных ресурсов',
              'Предложение дополнительных платных услуг УО',
              'Размещение новостей и отчётов',
              'Автоматическая синхронизация вашего сайта с ГИС ЖКХ',
              'Приём оплаты за ЖКУ',
          ]
      };
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}

.usage {
    display: flex;
    flex-direction: column;
    align-items: center;
    .container {
        width: 90%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        
        .main-title {
            font-size: 34px;
            text-transform: uppercase;
            font-weight: 700;
            color: #333;
            margin-top: 76px;
            text-align: center;
            width: 100%;
            font-family: "PT Sans", sans-serif;
        }
        .users {
            width: 100%;
            height: 44px;
            position: relative;
            max-width: 540px;
            margin-bottom: 25px;
            &-img {
                background: url(../assets/users-solid.svg);
                background-repeat: no-repeat;
                background-position: center;
                background-size: contain;
                height: 44px;
                width: 100px;
                margin-top: 13px;
                position: absolute;
                z-index: 3;
                left: 50%;
                margin-left: -50px;
                background-color: #fff;
            }
            &-bar::before {
                content: "";
                display: block;
                height: 2px;
                width: 100%;
                background-color: #de2b41;
                position: absolute;
                z-index: 2;
                top: 38px;
            }
        }

        .cons {
            display: flex;
            justify-content: center;
            align-items: center;

            .uc-tsg {
                height: 546px;
                margin: 0 -25px 0 -25px;
            }

            &-img {
                height: 676px;
                width: 331px;
                margin: 0 45px;
            }
            &-text-container {
                .cons-title {
                    font-size: 27px;
                    color: #046ab4;
                    font-weight: 700;
                    margin-top: 10px;
                    margin-bottom: 16px;
                    font-family: "PT Sans", sans-serif;
                }

                ul {
                    list-style: none;
                    padding: 0;
                    margin: 0;
                    li {
                        margin-left: -20px !important;
                        font-size: 18px;
                        line-height: 33px;
                        padding-left: 40px;
                        font-family: "PT Sans", sans-serif;
                        &::before {
                            content: "—";
                            margin: 0 5px 0 -20px !important;
                        }
                    }
                }

                .connect {
                    width: 350px;
                    margin-top: 33px;
                    padding: 0 18px;
                }
            }
        }
    }
}

</style>


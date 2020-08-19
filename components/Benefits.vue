<template>
  <section class="benefits">
      <div class="container">
          <!-- <img :src="items[0].img" alt=""> -->
          <div class="benefits-group" v-for="item in items" v-bind:key="item.id">
              <div class="bg-white-circle">
                  <img :class="item.classTitle" :src="item.img" alt="">
              </div>
              <div class="benefit-title">
                  {{item.title}}
              </div>
              <div class="benefit-text">
                  {{item.text}}
              </div>
          </div>
      </div>
  </section>
</template>

<script>
import mail from '../assets/mails.svg';
import conversation from '../assets/001-conversation.svg';
import multipleusers from '../assets/002-multiple-users.svg';

export default {
  components: {
  }, 
  data() {
      return {
          cls: 'mails',
          items: [
            {
                id: 1,
                img: mail,
                classTitle: 'mails',
                title: 'Информационная система',
                text: 'для улучшения коммуникации между жителями МКД и управляющей организацией'
            },
            {
                id: 2,
                img: conversation,
                classTitle: 'conversation',
                title: 'Обменивайтесь',
                text: 'с жителями МКД информацией и оперативно решайте вопросы управления МКД'
            },
            {
                id: 3,
                img: multipleusers,
                classTitle: 'multipleusers',
                title: 'Общайтесь',
                text: 'с управляющей организацией и ТСЖ, участвуйте в управлении своим домом'
            }
        ] 
      };
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}


.benefits {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 512px;
    min-height: 512px;
    background: #009cde;
    background-image: radial-gradient( circle farthest-side at center bottom, #0091d7, #004094 100% );
    color: #fff;

    .container {
        width: 90%;
        display: flex;
        align-items: center;

        .benefits-group {
            margin: 25px;
            display: flex;
            align-items: center;
            flex-direction: column;
            .bg-white-circle {
                height: 92px;
                width: 92px;
                border-radius: 50%;
                display: flex;
                justify-content: center;
                align-items: center;
                background-color: #fff;

                .mails {
                    height: 53px;
                    margin-left: 8px;
                }
                .multipleusers {
                    height: 62px;
                }
                .conversation {
                    height: 53px;
                }
            }
            .benefit-title {
                font-size: 26px;
                margin: 18px 0 8px;
                text-align: center;
                font-family: "PT Sans", sans-serif;
            }
            .benefit-text {
                font-size: 19px;
                text-align: center;
                line-height: 26px;
                font-family: "PT Sans", sans-serif;
            }
        }

    }
}

</style>


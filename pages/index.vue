<template>
  <v-container
    fluid
    class="main fill-height pa-0"
  >
    <v-row no-gutters>
      <v-col
        cols="12"
        class="cover mt-6 main__section px-6 px-sm-6 px-md-0 px-lg-0 px-xl-0"
      >
        <v-container class="section">
          <v-row class="mb-12">
            <v-col
              cols="12"
              sm="6"
              class="pa-0 mb-4 mb-sm-0"
            >
            <span class="cover__name font-weight-bold">
              {{ $t("name") }}<br>
              {{ $t("lastName") }}
            </span>
            </v-col>
            <v-col
              cols="12"
              sm="3"
              class="d-flex align-end font-weight-medium pa-0"
            >
              Frontend Developer<br>
              26 {{ $t("years") }}
            </v-col>
            <v-col
              cols="3"
              class="cover__box font-weight-bold pa-0 hidden-sm-and-down"
            >
              <span class="cover__lang">
                <v-btn
                  text
                  :class="{ 'cover__lang-item--not-active': notActive === 'en' }"
                  class="cover__lang-item"
                  @click="changeLanguage('ru')"
                >RU</v-btn>|
                <v-btn
                  text
                  @click="changeLanguage('en')"
                  :class="{ 'cover__lang-item--not-active': notActive === 'ru' }"
                  class="cover__lang-item"
                >ENG</v-btn>
              </span>
            </v-col>
          </v-row>

          <v-row justify="center">
            <img
              :src="require('~/assets/images/foto.jpg')"
              class="hidden-xs-only"
            >
            <img
              :src="require('~/assets/images/foto_mobile.jpg')"
              width="100%"
              class="hidden-sm-and-up"
            >
          </v-row>
        </v-container>
      </v-col>

      <v-col
        id="about"
        cols="12"
        class="about main__section"
      >
        <v-container class="section px-6 px-sm-6 px-md-0 px-lg-0 px-xl-0">
          <v-col cols="12">
            <v-row
              align="center"
              justify="center"
            >
              <v-col cols="12" md="6">
                <p class="about__title text-center font-weight-bold mb-5">{{ $t("about.title") }}</p>
                <p class="about__text text-center font-weight-medium mb-7">{{ $t("about.text1") }}</p>
                <p class="about__text text-center font-weight-medium mb-7">{{ $t("about.text2") }}</p>
                <p class="about__text text-center font-weight-medium mb-7">{{ $t("about.text3") }}</p>
              </v-col>
            </v-row>
          </v-col>
        </v-container>
      </v-col>

      <v-col
        id="skills"
        cols="12"
        class="skills main__section"
      >
        <v-container class="section px-5 px-sm-5 px-md-0 px-lg-0 px-xl-0">
          <div class="skills__title text-center font-weight-bold mb-5">
            {{ $t("skills.title") }}
          </div>
          <div class="skills__subtitle text-center font-weight-medium mb-11">
            {{ $t("skills.text") }}
          </div>
          <v-row class="mt-11 flex-column flex-sm-row flex-md-row flex-lg-row flex-xl-row justify-center align-center">
            <v-col
              v-for="(item, i) in icons"
              :key="i"
              cols="3"
              class="pa-0 d-flex flex-column justify-center align-center mb-6"
            >
              <img
                :src="require(`~/assets/images/${item.icon}.jpg`)"
                class="skills__icon mb-4"
              >
              <div class="skills__name font-weight-bold">
                {{ item.text }}
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-col>

      <v-col
        id="portfolio"
        cols="12"
        class="portfolio main__section"
      >
        <v-container class="section px-6 px-sm-6 px-md-0 px-lg-0 px-xl-0">
          <p class="portfolio__title text-center font-weight-bold mb-12">{{ $t("portfolio.title") }}</p>
          <div class="portfolio__item">
            <img
              :src="require('~/assets/images/rbroker/1.png')"
              class="portfolio__image mb-11 elevation-11"
            >
            <p
              class="portfolio__name font-weight-medium text-center"
              v-html="$t('portfolio.rbroker')"
            />
          </div>
          <div>
            <img
              :src="require('~/assets/images/rleader/1.png')"
              class="portfolio__image mb-11 elevation-11"
            >
            <p
              class="portfolio__name font-weight-medium text-center"
              v-html="$t('portfolio.rleader')"
            />
          </div>
        </v-container>
      </v-col>

      <v-col
        id="contacts"
        cols="12"
        class="contacts skills main__section"
      >
        <v-container class="section px-6 px-sm-6 px-md-0 px-lg-0 px-xl-0">
          <div class="skills__title text-center font-weight-bold mb-6">
            {{ $t("contacts.title") }}
          </div>
          <div
            v-html="$t('contacts.text1')"
            class="skills__subtitle text-center font-weight-medium mb-11">
          </div>
          <div class="text-center">
            <v-btn
              rounded
              color="black"
              dark
              href="https://t.me/dianaidd"
              target="_blank"
              class="contacts__btn font-weight-bold px-6 mb-12"
            >{{ $t("contacts.button") }}</v-btn>
          </div>
          <v-row class="justify-center align-center mt-6">
            <v-col
              cols="2"
              class="pa-0 d-flex flex-column justify-center align-center"
            >
              <v-btn
                icon
                tile
                href="https://www.linkedin.com/in/dianaid/"
                target="_blank"
              >
                <img
                  :src="require('~/assets/images/in.png')"
                  class="contacts__icon"
                >
              </v-btn>
            </v-col>
            <v-col
              cols="2"
              class="pa-0 d-flex flex-column justify-center align-center"
            >
              <v-btn
                icon
                href="https://github.com/DianaIdiatullina/"
                target="_blank"
              >
                <img
                  :src="require('~/assets/images/github.png')"
                  class="contacts__icon"
                >
              </v-btn>
            </v-col>
            <v-col
              cols="2"
              class="pa-0 d-flex flex-column justify-center align-center"
            >
              <v-btn
                icon
                tile
                href="https://www.instagram.com/haosperfection/"
                target="_blank"
              >
                <img
                  :src="require('~/assets/images/ig.png')"
                  class="contacts__icon"
                >
              </v-btn>
            </v-col>
          </v-row>
          <div
            class="contacts__text text-center font-weight-medium mt-7"
            v-html="$t('contacts.text2')"
          />
        </v-container>
      </v-col>

    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    notActive: 'ru',
    icons: [
      { text: 'Html', icon: 'html' },
      { text: 'Css', icon: 'css' },
      { text: 'Scss', icon: 'sass' },
      { text: 'Js', icon: 'js' },

      { text: 'Vue.js', icon: 'vue' },
      { text: 'Nuxt', icon: 'nuxt' },
      { text: 'Vuetify', icon: 'vuetify' },
      { text: 'Git', icon: 'git' },

      { text: 'Figma', icon: 'figma' },
      { text: 'Avocode', icon: 'avocode' },
      { text: 'Trello', icon: 'trello' },
      { text: 'Jest', icon: 'jest' }
    ],
  }),
  methods: {
    /**
     * Called when a language button is clicked
     * Changes the i18n context variable's locale to the one selected
     */
    changeLanguage(lang) {
      this.$i18n.locale = lang
      this.notActive = lang
    }
  }
}
</script>

<style lang="scss" scoped>

  .main {
    .cover {
      margin-bottom: 100px;

      &__name {
        font-size: 48px;
        line-height: 60px;
      }

      &__box {
        position: relative;
      }

      &__lang {
        transform: rotate(-90deg);
        position: absolute;
        right: -35px;
        bottom: 40px;

        &-item {
          font-size: 16px !important;
          color: #070707;
          font-family: Gilroy-Bold, sans-serif;
          font-weight: bold;
          padding: 0;
          height: 20px;
          min-width: 40px;

          &--not-active {
            color: #828282;
          }
        }
      }
    }

    .about {
      background: #F6F6F6;
      padding: 120px 0 100px 0 !important;

      &__title {
        font-size: 34px;
        line-height: 42px;
      }

      &__text {
        line-height: 22px;
        font-family: Gilroy-Medium, sans-serif;
      }
    }

    .skills {
      padding: 90px 0 110px 0 !important;

      &__title {
        font-size: 34px;
        line-height: 42px;
      }

      &__subtitle {
        font-family: Gilroy-Medium, sans-serif;
      }

      &__icon {
        max-height: 88px;
        max-width: 88px;
      }

      &__name {
        font-size: 14px;
        line-height: 17px;
        color: #828282;

      }
    }

    .portfolio {
      background: #F6F6F6;
      padding: 110px 0 90px 0 !important;

      &__title {
        font-size: 34px;
        line-height: 42px;
      }

      &__text {
        line-height: 22px;
        font-family: Gilroy-Medium, sans-serif;
      }

      &__image {
        max-width: 100%;
      }

      &__name {
        font-family: Gilroy-Medium, sans-serif;
      }

      &__item {
        margin-bottom: 110px;
      }
    }

    .contacts {
      &__btn {
        text-transform: none;
        height: 42px !important;
      }

      &__icon {
        max-height: 40px;
        max-width: 40px;
      }

      &__text {
        font-size: 14px;
        font-family: Gilroy-Medium, sans-serif;
        color: #828282;
      }
    }

    @media (max-width: 959px) {
      .about {
        padding: 81px 0 76px 0 !important;
      }

      .cover {
        padding-top: 40px;
        margin-bottom: 83px;
      }

      .skills {
        padding: 83px 0 98px 0 !important;
      }

      .portfolio {
        padding: 81px 0 80px 0 !important;

        &__item {
          margin-bottom: 77px;
        }
      }
    }
  }
</style>

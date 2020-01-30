<template>
  <v-container
    fluid
    class="main fill-height pa-0"
  >
    <v-row no-gutters>
      <v-col
        cols="12"
        class="cover"
      >
        <v-container class="section pa-0">
          <v-row class="mb-12">
            <v-col
              cols="6"
              class="pa-0"
            >
            <span class="cover__name font-weight-bold">
              Diana<br>
              Idiatullina
            </span>
            </v-col>
            <v-col
              cols="3"
              class="d-flex align-end font-weight-medium pa-0"
            >
              Frontend Developer<br>
              26 years old, Minsk
            </v-col>
            <v-col
              cols="3"
              class="cover__box font-weight-bold pa-0"
            >
              <span class="cover__lang"><span class="cover__lang--not-active">RU</span> | ENG</span>
            </v-col>
          </v-row>

          <v-row>
            <img :src="require('~/assets/images/foto.jpg')">
          </v-row>
        </v-container>
      </v-col>

      <v-col
        cols="12"
        class="about"
      >
        <v-row
          align="center"
          justify="center"
        >
          <v-col cols="12" md="5" lg="4">
            <p class="about__title text-center font-weight-bold mb-5">About me</p>
            <p class="about__text text-center font-weight-medium mb-7">Hi, I'm Denis – UX/UI designer from Minsk.<br>I'm interested in design and everything connected with it.</p>
            <p class="about__text text-center font-weight-medium mb-7">I'm studying at courses "Web and mobile design interfaces" in IT-Academy.</p>
            <p class="about__text text-center font-weight-medium mb-7">Ready to implement excellent projects with wonderful people.</p>
          </v-col>
        </v-row>
      </v-col>

      <v-col
        cols="12"
        class="skills"
      >
        <v-container class="section pa-0">
          <div class="skills__title text-center font-weight-bold mb-5">
            Skills
          </div>
          <div class="skills__subtitle text-center font-weight-medium mb-11">
            I work with such technologies as
          </div>
          <v-row class="mt-11">
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
        cols="12"
        class="portfolio"
      >
        <v-row
          align="center"
          justify="center"
        >
          <v-col cols="12" md="5" lg="4">
            <p class="portfolio__title text-center font-weight-bold mb-5">Portfolio</p>
          </v-col>
        </v-row>
      </v-col>

    </v-row>
  </v-container>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  data: () => ({
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
  components: {
    Logo
  }

}
</script>

<style lang="scss">

  @media (min-width: 1264px) {
    .section {
      max-width: 940px !important;
    }
  }

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
      font-size: 16px;
      position: absolute;
      right: -16px;
      bottom: 35px;

      &--not-active {
        color: #828282;
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
  }

</style>

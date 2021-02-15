<template>
  <div class="header-menu d-none d-sm-flex">
    <v-container class="section">
      <v-row
        justify="space-between"
        class="pa-4 flex-nowrap"
      >
        <v-col cols="auto" class="pa-0">
          <a
            href="#home"
            @click="isActive = 'home'"
            :class="{ 'header-menu__item--active': isActive === 'home' }"
            class="header-menu__item font-weight-bold"
          >
            Home
          </a>
        </v-col>
        <v-col cols="auto" class="pa-0">
          <a
            href="#about"
            @click="isActive = 'about'"
            :class="{ 'header-menu__item--active': isActive === 'about' }"
            class="header-menu__item font-weight-bold"
          >
            About me
          </a>
        </v-col>
        <v-col cols="auto" class="pa-0">
          <a
            href="#skills"
            @click="isActive = 'skills'"
            :class="{ 'header-menu__item--active': isActive === 'skills' }"
            class="header-menu__item font-weight-bold"
          >
            Skills
          </a>
        </v-col>
        <v-col cols="auto" class="pa-0">
          <a
            href="#portfolio"
            @click="isActive = 'portfolio'"
            :class="{ 'header-menu__item--active': isActive === 'portfolio' }"
            class="header-menu__item font-weight-bold"
          >
            Portfolio
          </a>
        </v-col>
        <v-col cols="auto" class="pa-0">
          <a
            href="#contacts"
            @click="isActive = 'contacts'"
            :class="{ 'header-menu__item--active': isActive === 'contacts' }"
            class="header-menu__item font-weight-bold"
          >
            Contacts
          </a>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
  export default {
    data: () => ({
      isActive: 'home'
    })
  }
</script>

<style lang="scss" scoped>

  .header-menu {
    border-bottom: 1px solid #828282;
    background: #fff;
    z-index: 100;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;

    &__item {
      color: #828282;
      text-decoration: none;

      &--active {
        color: #070707;
      }
    }
  }
</style>

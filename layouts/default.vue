<template>
  <v-app>
    <div
      id="home"
      class="page"
    >
      <header-menu/>
      <v-content>
        <nuxt/>
      </v-content>
    </div>
  </v-app>
</template>

<script>
  import HeaderMenu from '~/components/HeaderMenu.vue'

  export default {
    components: {
      HeaderMenu
    }
  }
</script>

<style>
  .page {
    padding-top: 83.5px;
  }

  @media (max-width: 959px) {
    .page {
      padding-top: 0;
    }
  }
</style>



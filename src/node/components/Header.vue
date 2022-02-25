<template>
  <v-app-bar color="#B0D0E8" app>
    <v-row align="center" justify="center" no-gutters>
      <v-col :cols="2">
        <v-btn to="/" block nuxt color="#fff" text class="mr-2">HOME</v-btn>
      </v-col>
      <v-col :cols="2">
        <v-btn to="/articles" block nuxt color="#fff" text class="mr-2">BLOG</v-btn>
      </v-col>
      <v-col :cols="2">
        <v-btn to="/" block nuxt color="#fff" text>HOW</v-btn>
      </v-col>
      <v-col :cols="2">
        <v-btn to="/" block nuxt color="#fff" text>留意点</v-btn>
      </v-col>
      <v-col :cols="4" align-self="center">
        <v-img src="/vuetify-logo.svg" max-height="60px" contain></v-img>
      </v-col>

    </v-row>
  </v-app-bar>
</template>

<script>
export default {
  name: "Header",
}
</script>

<style scoped lang="scss">
.v-toolbar__content {
  z-index: 10 !important;
}
</style>

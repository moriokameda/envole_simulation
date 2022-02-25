<template>
  <v-footer color="#B0D0E8" class="mt-20">
    <v-row no-gutters align="" justify="">
      <v-col sm="4" md="4" align-self="center" cols>
        <v-img src="/vuetify-logo.svg" max-height="60px" contain></v-img>
      </v-col>
      <v-col sm="3" md="2" cols>
        <v-btn to="/privacy" block nuxt color="#fff" text class="mr-2 font-weight-bold">プライバシーポリシー</v-btn>
      </v-col>
      <v-col sm="3" md="2" cols>
        <v-btn to="/notation" block nuxt color="#fff" text class="font-weight-bold">特定商取引に基づく表記</v-btn>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped>

</style>

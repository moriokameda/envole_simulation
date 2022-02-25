<template>
  <div class="my-50 position_relative">
    <v-row align="center" justify="center">
      <v-col sm="9" offset="">
        <h2 class="font-40" style="z-index: 5">たったの３STEP</h2>
      </v-col>
    </v-row>
    <v-row class="position_relative " no-gutters align="start" justify="center">
      <vue-wavify fill="#B0D0E8" class="position_absolute wave">
        <defs></defs>
      </vue-wavify>
      <v-col offset-sm="6" sm="6" cols="10" class="position_absolute ship_position">
        <v-img src="/ship.png" contain width="" position="center center" max-width="200px"></v-img>
      </v-col>
      <v-col sm="6" cols="10" class="mt-10 wave-content position_relative" align-self="center">
        <h2 class="text-center text--white font-weight-bold font-40">STEP1</h2>
        <v-row no-gutters justify="center">
          <v-col sm="8" md="6" cols="12" class="mt-10">
            <p class="text--white">テストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテスト</p>
            <v-img class="position_absolute fish_position" src="/fish.png" max-width="100px"></v-img>
          </v-col>
        </v-row>

      </v-col>
      <v-col sm="6" order="1" cols="11" class="wave-content mt-15">
        <h2 class="font-weight-bold font-40 color-blue text-center">シミュレーション方法</h2>
      </v-col>
    </v-row>
    <v-row class="position_relative" no-gutters justify="center">
      <vue-wavify fill="#64A1CE" class="position_absolute wave">
        <defs></defs>
      </vue-wavify>
      <v-col offset-sm="6" sm="6" cols="10" class="wave-content mt-10 position_relative">
        <h2 class="text-center text--white font-weight-bold font-40">STEP2</h2>
        <v-row no-gutters justify="center">
          <v-col sm="8" md="6" cols="12" class="mt-10">
            <p class="text--white">テストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテスト</p>
            <v-img class="position_absolute fish_position2" src="/fish2.png" max-width="100px"></v-img>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row class="position_relative" no-gutters justify="center">
      <vue-wavify fill="#2F6791" mask="" class="position_absolute wave">
        <defs></defs>
      </vue-wavify>
      <v-col sm="6" cols="10" class="wave-content mt-10 position_relative">
        <h2 class="text-center text--white font-weight-bold font-40">STEP3</h2>
        <v-row no-gutters justify="center">
          <v-col sm="8" md="6" cols="12" class="mt-10">
            <p class="text--white">テストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテスト</p>
          </v-col>
        </v-row>
        <v-row no-gutters align="end" justify="center" class="position_relative">
          <v-col sm="6" cols="11">
            <v-img class="position_absolute fish_position3" src="/fish3.png" max-width="300px"></v-img>
          </v-col>
        </v-row>
      </v-col>
      <v-col sm="6"></v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "SimulationStep"
}
</script>

<style scoped lang="scss">
</style>

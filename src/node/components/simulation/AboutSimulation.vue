<template>
  <div class="mt-50">
    <v-row no-gutters class="bk-color-green" align="center" justify="center">
      <v-col md="7" cols="12" class="polygon-right-point bk-color-light-blue py-10" align-self="center">
        <v-row no-gutters justify="center">
          <v-col md="9" cols="12">
            <h3 class="text-center text--white mt-30 font-40 mobile-font-20em">シミュレーションとは</h3>
            <div class="text-center text--white" style="max-width: 70%; margin: 30px auto">テストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテス</div>
          </v-col>
          <v-col md="3"></v-col>
        </v-row>

      </v-col>
      <v-col md="5" cols="11" class="position_relative bk-color-green py-10" align-self="center">
        <v-row no-gutters justify="center">
          <v-col offset-sm="9" sm="3" cols="3">
            <v-img src="/light.png" max-width="100px" position="center center"></v-img>
          </v-col>
        </v-row>
        <h3 class="text-center text--white font-weight-bold font-size-large mobile-font-15em">探しているものがすぐ見つかる</h3>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "AboutSimulation"
}
</script>

<style scoped lang="scss">
.polygon-right-point {
  clip-path: polygon(0% 0%, 75% 0%, 100% 50%, 75% 100%, 0% 100%);
}
@media screen and (max-width: 768px){
  // polygon
  .polygon-right-point {
    clip-path: border-box !important;
  }
}
</style>

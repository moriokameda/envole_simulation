<template>
  <v-container class="mt-16">
    <v-row align="center" justify="center">
      <v-col>
        <div class="align-center text-center">
          <span class="line">\</span><span class="message">あなたにぴったりなものをシミュレーション</span><span class="line">/</span>
        </div>
      </v-col>
    </v-row>
    <v-row align="center" justify="center" class="mt-5">
      <h2 class="text-center text-title">シミュレーション</h2>
    </v-row>
    <v-row align="center" justify="center" class="mt-20" no-gutters>
      <v-col sm="8">
        <p>
          テストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテスト
        </p>
      </v-col>
    </v-row>
    <v-row id="whichItem" align="center" justify="center">
      <h2 class="text-center font-40 color-blue">あなたが探しているのはどっち？</h2>
    </v-row>
    <v-row align="center" no-gutters justify="center" class="mt-20">
      <v-col sm="3" class="position_relative mobile-mt-10" cols="10" align-self="center">
        <v-img src="/sao.png" class="position_absolute" max-width="150px" height="100px" style="left: -4rem;top: -20px; z-index: 2; object-fit: cover" ></v-img>
        <v-btn elevation="5" x-large color="#BCD537" class="position_relative pa-8" block href="#rod">
          <span class="text--white font-weight-bold font-29">竿(ロッド)</span>
          <div class="rotate-icon">
            <v-icon color="#2F6791" x-large>mdi-play</v-icon>
          </div>
        </v-btn>
      </v-col>
      <v-col class="position_relative mobile-mt-10" sm="3" offset-sm="1" cols="10" align-self="center">
        <v-img src="/reel.png" class="position_absolute" width="150px" height="100px" style="left: -4rem;top: -20px; z-index: 2"></v-img>
        <v-btn elevation="5" x-large color="#64A1CE" block class="pa-8" href="#reel">
          <span class="text--white font-weight-bold font-29">リール</span>
          <div class="rotate-icon size-large">
            <i class="fa-solid fa-magnifying-glass"></i>
          </div>
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "SimulationNarration"
}
</script>

<style scoped>

</style>

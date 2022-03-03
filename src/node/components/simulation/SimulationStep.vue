<template>
  <div class="my-50 position_relative">
    <v-row align="center" justify="center" no-gutters class="mb-10">
      <v-col sm="9" offset="">
        <h2 class="font-40 text-center" style="z-index: 5">たったの３STEP</h2>
      </v-col>
    </v-row>
    <v-row class="position_relative mobile-mt-20" no-gutters align="start" justify="center">
      <vue-wavify fill="#B0D0E8" class="position_absolute wave">
        <defs></defs>
      </vue-wavify>
      <v-col offset-sm="6" sm="6" cols="10" class="position_relative">
        <v-img src="/ship.png" contain position="center center" min-width="100px" min-height="100px" max-width="200px" class="position_absolute ship_position"></v-img>
      </v-col>
      <v-col sm="6" cols="10" class="mt-10 wave-content position_relative" align-self="center">
        <h2 class="text-center text--white font-weight-bold font-40">STEP1</h2>
        <v-row no-gutters justify="center" align="center">
          <v-col sm="8" md="6" cols="12" class="mt-10">
            <p class="text--white">テストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテストテテストテストテストテストテスト</p>
            <v-img class="position_absolute fish_position" src="/fish.png" max-width="100px"></v-img>
          </v-col>
        </v-row>

      </v-col>
      <v-col sm="6" order="1" cols="11" class="wave-content mt-30 mobile-mt-0">
        <h2 class="font-weight-bold font-size-large color-blue text-center">シミュレーション方法</h2>
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
// how to simulation
.ship_position {
  top: -5em;
  right: 5em;
  z-index: 5;
  animation: ship_animation;
  animation-timing-function: ease-in-out;
  animation-iteration-count: infinite;
  //animation-direction: alternate;
  animation-duration: 3.2s;
}
.fish_position {
  top: 3rem;
  right: 2rem;
  animation: fish_animation;
  animation-timing-function: ease-in-out;
  animation-iteration-count: infinite;
  animation-duration: 5s;
}
.fish_position2 {
  top: 0;
  right: 10rem;
  animation: fish_animation2;
  animation-timing-function: ease-in-out;
  animation-iteration-count: infinite;
  animation-duration: 5s;
}
.fish_position3 {
  top: -1.5rem;
  right: 1rem;
}
@keyframes ship_animation {
  0% {top: -5em; right: 5em;}
  100% {top: 20em; right: 7em; transform: rotate(180deg);}
}
@keyframes fish_animation {
  0% {top: 3rem; right: 2rem;}
  //50% {top: 5rem; right: -5rem; transform: rotate(-30deg)}
  100% {top: 20rem; right: -101vw; transform: rotate(-30deg)}
}
@keyframes fish_animation2 {
  0%{top: 0; right: 10rem;}
  //50% {top: 2rem; right: 15rem;}
  100% {top: 40rem; right: 101vw;}
}

@media screen and (max-width: 768px){
  .ship_position {
    right: 0;
  }
  .fish_position {
    top: 2rem;
    right: 0;
    left: 0;
  }
  .fish_position2 {
    right: 0;
  }
}
</style>

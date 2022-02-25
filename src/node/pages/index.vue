<template>
  <div class="main">
    <simulation-top></simulation-top>
    <simulation-narration></simulation-narration>
    <about-simulation></about-simulation>
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
    <run-simulation
      item-slug="rod"
      search-result-text="ぴったりな竿を見つけました"
      card-color="#BCD537"
      :searched-items="rods"
      search-before-text="あなたの竿をお探します"
      border-class="border-green"
      bk-color-class="bk-color-green"
      search-item-icon="/rod2.png"
      class="mt-50"
    ></run-simulation>
    <run-simulation
      item-slug="reel"
      search-result-text="ぴったりなリールを見つけました"
      card-color="#B0D0E8" :searched-items="reels"
      search-before-text="あなたのリールをお探しします"
      border-class="border-light-blue"
      bk-color-class="bk-color-light-blue"
      search-item-icon="/reel.png"
      class="my-50"
    ></run-simulation>
  </div>
</template>

<script>
import {mdiChevronDown} from '@mdi/js';
import SimulationTop from "~/components/simulation/SimulationTop";
import AboutSimulation from "~/components/simulation/AboutSimulation";
import SimulationNarration from "~/components/simulation/SimulationNarration";
import RunSimulation from "~/components/simulation/RunSimulation";

export default {
  name: 'NuxtIndexPage',
  comments: {
    mdiChevronDown,
  },
  components: {
    RunSimulation,
    SimulationNarration,
    AboutSimulation,
    SimulationTop,
  },
  data() {
    return {
      rods: [
        {cost: 7850, title: "DAIWA リバティクラブ 磯風 3号-45遠投・K911627", key: 1, src: '/sao.png'},
        {cost: 6120, title: "テストロッド１", key: 2, src: '/sao.png'},
        {cost: 15480, title: "テストロッド2", key: 3, src: '/sao.png'},
        {cost: 13580, title: "テストロッド3", key: 4, src: '/sao.png'},
        {cost: 25080, title: "テストロッド4", key: 5, src: '/sao.png'},
        {cost: 3940, title: "テストロッド5", key: 6, src: '/sao.png'},
        {cost: 14570, title: "テストロッド6", key: 7, src: '/sao.png'},
      ],
      reels: [
        {cost: 7850, title: "テストリール1", key: 1, src: '/reel.png'},
        {cost: 6180, title: "テストリール2", key: 2, src: '/reel.png'},
        {cost: 7850, title: "テストリール3", key: 3, src: '/reel.png'},
        {cost: 7850, title: "テストリール4", key: 4, src: '/reel.png'},
        {cost: 7850, title: "テストリール5", key: 5, src: '/reel.png'},
      ],

    }
  },
}
</script>
<style lang="scss">
.header-carousel .v-carousel__controls {
  justify-content: right;
  right: 10vw !important;
}

.message {
  margin-left: 1rem;
  margin-right: 1rem;
  font-size: 1.5em;
}

span.line {
  font-size: 3rem;
  font-weight: lighter;
}

h2.text-title {
  font-size: 40px;
  font-family: "Tsukushi A Round Gothic", "Noto sans";
}

.left {
  left: 0;
}

.text--white {
  color: #fff;
}

.rotate-icon {
  border-radius: 50%;
  background-color: #fff;
}

.polygon-right-point {
  clip-path: polygon(0% 0%, 75% 0%, 100% 50%, 75% 100%, 0% 100%);
}

.theme--light.v-chip {
  border-color: #BCD537;
}

.theme--light.v-chip:not(.v-chip--active) {
  background-color: #fff;
}

.ship_position {
  top: -5em;
  right: -15em;
  z-index: 3;
}
.fish_position {
  top: 3rem;
  right: 2rem;
}
.fish_position2 {
  top: 0;
  right: 5rem;
}
.fish_position3 {
  top: -1.5rem;
  right: 1rem;
}
.wave {
  z-index: 1;
}
.wave-content {
  z-index: 5;
}
.vue-wavify-wave svg {
  height: 450px !important;
}
</style>

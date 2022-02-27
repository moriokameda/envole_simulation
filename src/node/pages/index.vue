<template>
  <div class="main">
    <simulation-top></simulation-top>
    <simulation-narration></simulation-narration>
    <about-simulation></about-simulation>
    <simulation-step></simulation-step>
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
import SimulationStep from "~/components/simulation/SimulationStep";

export default {
  name: 'NuxtIndexPage',
  comments: {
    mdiChevronDown,
  },
  components: {
    SimulationStep,
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

span.line {
  font-size: 3rem;
  font-weight: lighter;
}

.message {
  margin-left: 1rem;
  margin-right: 1rem;
  font-size: 1.5em;
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

.theme--light.v-chip {
  border-color: #BCD537;
}

.theme--light.v-chip:not(.v-chip--active) {
  background-color: #fff;
}
@media screen and (max-width: 768px){
  .message {
    font-size: 1.2em;
  }
  span.line {
    font-size: 2rem;
  }
}

</style>

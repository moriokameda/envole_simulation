<template>
  <v-container :id="itemSlug" class="mt-30">
    <v-row align="center" justify="center" class="position_relative">
      <v-col sm="5" md="4" cols="7" class="position_absolute">
        <v-img :src="searchItemIcon" width="100%" position="center center" max-width="100%" contain height="200px"></v-img>
      </v-col>
      <v-col cols="10" class="mt-40">
        <h2 class="font-weight-bold font-size-large text-center">{{searchBeforeText}}</h2>
      </v-col>
    </v-row>
    <v-row align="center" justify="center" class="mt-10">
      <v-col align-self="center">
        <v-form ref="form" align="center">
          <p class="text-center font-weight-bold font-15em">ご希望の予算</p>
          <v-chip-group v-model="rodCost" background-color="#fff" color="#0c0c0c" align="center" mandatory column>
            <v-row no-gutters align="center" justify="center">
              <v-col>
                <v-chip
                  v-for="cost in costs"
                  :key="cost.key"
                  :value="cost.value"
                  class="font-12em"
                  :class="borderClass"
                  :active-class="bkColorClass"
                  :style="styles"
                >
                  <span class="color-black font-noto-sans-cjk font-15em">{{ cost.key }}</span></v-chip>
              </v-col>
            </v-row>
          </v-chip-group>
          <p class="text-center font-weight-bold font-15em">欲しい種類</p>
          <v-chip-group v-model="rodType" background-color="#fff" color="#0c0c0c" align="center" column>
            <v-row no-gutters align="center" justify="center">
              <v-col>
                <v-chip
                  v-for="type in types"
                  :key="type.key"
                  :value="type.value"
                  class="font-12em"
                  :class="borderClass"
                  :active-class="bkColorClass"
                  :style="styles"
                >
                  <span class="color-black font-noto-sans-cjk font-15em">{{ type.key }}</span></v-chip>
              </v-col>
            </v-row>
          </v-chip-group>
          <p class="text-center font-weight-bold font-15em">狙いたい魚</p>
          <v-chip-group v-model="wantFish" background-color="#fff" color="#0c0c0c" align="center" column>
            <v-row no-gutters align="center" justify="center">
              <v-col>
                <v-chip
                  v-for="fish in fishes"
                  :key="fish.key"
                  :value="fish.value"
                  class=" font-12em"
                  :class="borderClass"
                  :active-class="bkColorClass"
                  :style="styles"
                >
                  <span class="color-black font-noto-sans-cjk font-15em">{{ fish.key }}</span></v-chip>
              </v-col>
            </v-row>
          </v-chip-group>
<!--          <v-btn rounded color="#64A1CE" class="mt-10 font-15em" x-large fab @click="searchRods">検索<br>START</v-btn>-->
          <v-btn rounded color="#64A1CE" class="mt-15 font-15em" x-large fab @click="searchRods">
            <v-img src="/startSearch.png" contain max-width="200px"></v-img>
          </v-btn>
        </v-form>
      </v-col>
    </v-row>
    <v-row align="center" justify="center" class="mt-20">
      <v-col>
        <div class="align-center text-center">
          <span class="line">\</span><span class="message font-weight-bold">{{searchResultText}}</span><span class="line">/</span>
        </div>
      </v-col>
    </v-row>
    <v-row align="center" justify="center" class="mt-10" no-gutters>
      <client-only>
        <carousel-3d count="2" controls-visible="true" :width="400" :height="600" :style="styles">
          <slide v-for="(item, index) in searchedItems" :key="item.key" :index="index" class="border-radius-5">
            <v-card :color="cardColor" max-width="100%" width="100%" height="100%">
              <v-sheet color="#fff" class="mt-10 mr-5 ml-5">
                <v-card-title class="color-black">{{ item.title }}</v-card-title>
              </v-sheet>
              <v-sheet class="mt-10 mr-5 ml-5">
                <v-img :src="item.src" max-width="300px" max-height="300px" contain></v-img>
              </v-sheet>
              <v-sheet class="my-10 mx-5">
                <v-card-text>
                  {{ item.cost }}円(税込)
                </v-card-text>
              </v-sheet>
            </v-card>
          </slide>
        </carousel-3d>
      </client-only>

    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "RunSimulation",
  props: {
    itemSlug: {
      type: String,
      required: true
    },
    searchBeforeText: {
      type: String,
      required: true,
    },
    searchResultText: {
      type: String,
      required: true
    },
    cardColor: {
      type: String,
      required: true,
    },
    searchedItems: {
      type: Array,
      required: false,
      // eslint-disable-next-line vue/require-valid-default-prop
      default: [{key: 1, title: "", cost: 0, src: "/sao.png"}],
    },
    borderClass: {
      type: String,
      required: true,
    },
    bkColorClass: {
      type: String,
      required: true,
    },
    searchItemIcon: {
      type: String,
      required: true,
    }
  },
  data() {
    return {
      rodCost: 0,
      costs: [
        {key: "~¥5,000", value: 1},
        {key: "¥5,000~¥5,000", value: 2},
        {key: "¥15,000~¥30,000", value: 3},
        {key: "¥30,000~", value: 4},
      ],
      rodType: 0,
      types: [
        {key: "ペイト", value: 1},
        {key: "スピニング", value: 2},
        {key: "分からない", value: 3},
      ],
      wantFish: 0,
      fishes: [
        {key: "大物", value: 1},
        {key: "普通", value: 2},
        {key: "小物", value: 3},
      ],
    }
  },
  computed: {
    styles() {
      return {
        '--color': this.cardColor
      }
    }
  },
  methods: {
    searchRods(e) {
      // eslint-disable-next-line no-console
      console.log(e);
      // eslint-disable-next-line no-console
      console.log(this.rodType)
    }
  },
}
</script>

<style scoped lang="scss">
.carousel-3d-slide {
  //background-color: #B0D0E8;
  background-color: var(--color);
}
.theme--light.v-chip {
  border-color: var(--color);
}


</style>

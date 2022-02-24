<template>
  <div class="header-carousel">
    <v-carousel
      continuous
      :show-arrows="false"
      hide-delimiter-background
      height="60vh"
    >
      <v-carousel-item
        v-for="(item, i) in carouselItems"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
        <v-sheet height="100%" color="rgba(225,255,255,0)">
          <v-row no-gutters class="carousel-top">
            <v-col :offset="1" :sm="8">
              <span class="furigana">もの</span>
              <div class="text--white title_carousel">あなたに合った最高に出会える場所</div>
            </v-col>
          </v-row>
          <v-row justify="center" align="end" class="bottom-height">
            <v-col cols="auto">
              <span class="text--white font-size-large font-noto-sans text-center">SIMULATION START</span>
            </v-col>
          </v-row>
          <v-row justify="center" align="end" class="">
            <v-col cols="auto">
              <v-icon class="material-icons" size="9rem" color="#fff">mdi-chevron-down</v-icon>
            </v-col>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
import {mdiChevronDown} from "@mdi/js";

export default {
  name: "SimulationTop",
  comments: {
    mdiChevronDown,
  },
  data() {
    return {
      carouselItems:[
        {
          src: "/carousel1.jpg"
        },
        {
          src: "/img.png"
        },
      ]
    }
  },
}
</script>

<style scoped lang="scss">
.header-carousel .v-carousel__controls {
  justify-content: right;
  right: 10vw !important;
}
.header-carousel .carousel-top {
//margin-top: 10vw;
  margin-top: 50px;
  position: relative;
  .text--white {
    font-size: 3em;
  }
}
.text--white {
  color: white;
  font-family: "Tsukushi A Round Gothic";
//font-size: 52px;
//font-size: 3.8vw;
  font-weight: 700;
}
.title_carousel {
//max-width: 38vw;
  max-width: 520px;
}
.furigana {
  color: #eee;
  position: absolute;
  padding-left: 23em;
  top: -10px;
  letter-spacing: 1em;
}
.bottom-height {
  height: 40%;
}
@media screen and (max-width: 768px){
  .header-carousel .carousel-top {
    margin-top: 125px;
    .text--white {
      font-size: 26px;
    }
  }
  .text--white {
    font-size: 26px;
  }
  .furigana {
    font-size: 12px;
    padding-left: 190px;
    padding-bottom: 0;
    margin-bottom: 0;
    top: -10px;
    letter-spacing: 10px;
  }
  .v-carousel {
    height: 500px !important;
  }
  .v-window__container {
    height: 500px !important;
  }
  .bottom-height {
    height: 200px;
  }

}
</style>

<template>
  <v-app>
    <swiper class="swiper">
      <swiper-slide v-for="event in events" :key="event.name">
        <Counter :event="event" />
      </swiper-slide>
    </swiper>
  </v-app>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";
import Counter from "./components/Counter.vue";

export default {
  name: "app",
  components: {
    Swiper,
    SwiperSlide,
    Counter,
  },
  data() {
    return {
      events: [
        {
          name: "Maroon5",
          date: new Date(2022, 4, 9),
          hype: "זזים כמו ג'גר",
        },
        {
          name: "Imagine Dragons",
          date: new Date(2022, 4, 29),
          hype: "עפים בכיוונים שונים",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@font-face {
  font-family: "AlmoniBold";
  src: url("./../fonts/Almoni/ALMONI-NEUE-TZAR-AAA-800.TTF");
}

@font-face {
  font-family: "AlmoniRegular";
  src: url("./../fonts/Almoni/ALMONI-NEUE-TZAR-AAA-400.TTF");
}

@font-face {
  font-family: "AlmoniLight";
  src: url("./../fonts/Almoni/ALMONI-NEUE-TZAR-AAA-200.TTF");
}

.v-application--wrap {
  background-color: #554ab0;
  color: #c1b9ff;
}

body,
html {
  padding: 0 !important;
  margin: 0;
  width: 100vw;
  overflow: hidden;
  height: 100vh;
}

canvas {
  z-index: 30;
  position: absolute;
  top: 0;
  height: 100vh;
  width: 100vw;
  pointer-events: none;
}

.swiper {
  height: 100%;
  width: 100%;

  .swiper-slide {
    height: 100%;
    width: 100%;
    position: relative;
  }
}
</style>
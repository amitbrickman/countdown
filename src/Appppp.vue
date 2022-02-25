<template>
  <div id="app">
    <!-- <v-app>
      <swiper class="swiper" ref="mySwiper" :options="swiperOptions">
        <swiper-slide>Slide 1</swiper-slide>
        <swiper-slide>Slide 2</swiper-slide>
        <swiper-slide>Slide 3</swiper-slide>
        <swiper-slide>Slide 4</swiper-slide>
        <swiper-slide>Slide 5</swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
      <swiper ref="swiperComponentRef" :options="swiperOption" class="swiper">
        <swiper-slide v-for="event in events" :key="event">
          {{ event }}
        </swiper-slide>
      </swiper>
    </v-app> -->
  </div>
</template>

<script>
// import Counter from "./components/Counter.vue";
// import { Swiper, SwiperSlide } from "vue-awesome-swiper";

// export default {
//   name: "App",
//   components: {
//     // Counter,
//     // Swiper,
//     // SwiperSlide,
//   },
//   data() {
//     return {
//       events: ["imagine", "maroon"],
//       swiperOption: {
//         effect: "coverflow",
//         grabCursor: true,
//         centeredSlides: true,
//         slidesPerView: 1,
//         coverflowEffect: {
//           rotate: 0,
//           stretch: 0,
//           depth: 100,
//           modifier: 1,
//           slideShadows: false,
//         },
//         freeMode: true,
//       },
//     };
//   },
// };
</script>

<style>
/* @font-face {
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

swiper-slide {
  width: 70vw;
  background-color: red;
  width: 75vw;
  height: 70vh;
}

.swiper {
  height: 100%;
  width: 100%;
}

body,
html {
  padding: 0;
  margin: 0;
  width: 100vw;
  overflow: hidden;
  /* font-family: "Heebo"; */
  height: 100vh;
}

html {
  padding: 0px !important;
}

.v-application {
  /* font-family: "Pa" !important; */
}

canvas {
  z-index: 30;
  position: absolute;
  top: 0;
  height: 100vh;
  width: 100vw;
  pointer-events: none;
}

.v-application--wrap {
  width: 100vw;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  background-color: #554ab0;
  color: #c1b9ff;
}

p {
  margin: 0px !important;
  padding: 0px !important;
}

#status {
  font-family: "AlmoniBold";
  font-size: 28vh;
  line-height: 0.9;
  font-weight: 700;
  color: #eca4b8;
  text-shadow: 0 1px 0 #d84c76, 0 2px 0 #d84c76, 0 3px 0 #d84c76,
    0 4px 0 #d84c76, 0 5px 0 #d84c76, 0 6px 0 #d84c76, 0 7px 0 #d84c76,
    0 8px 0 #d84c76, 0 9px 0 #d84c76, 0 10px 0 #d84c76, 0 11px 0 #d84c76,
    0 12px 0 #d84c76, 0 20px 30px rgba(0, 0, 0, 0.5);
}

#name {
  font-size: 7vh;
  line-height: 0.2;

  font-family: "AlmoniRegular";
}

#office {
  font-size: 7vh;
  font-family: "AlmoniRegular";
  /* margin-top: 2vh !important; */
}

#holder {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: -15vh;
}

.vs-switch__text {
  font-size: 2vh;
  font-family: "AlmoniLight";
  letter-spacing: 0.3ch;
}

.vs-switch__circle {
  background-color: #eca4b8;
}

.off {
  color: #d84c76;
  font-weight: bold;
}

.on {
  font-weight: bold;
}

#toggle {
  position: absolute;
  bottom: 20vh;
  transform: scale(1.5);
} */
</style>

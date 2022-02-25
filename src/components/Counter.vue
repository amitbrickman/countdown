<template>
  <div id="holderholder">
    <div class="event-name">{{ event.name }}</div>
    <div id="holder">
      <div>
        <p id="name">עוד</p>
      </div>
      <div>
        <p id="status">{{ countdown }}</p>
      </div>
      <div>
        <p id="office">ימים עד ש{{ event.hype }}</p>
      </div>
    </div>
    <vs-switch id="toggle" color="#da4d77" @change="toggleStatus">
      <template #off>וויפייי </template>
      <template #on> יאייי </template>
    </vs-switch>
  </div>
</template>

<script>
const confetti = require("canvas-confetti");
export default {
  name: "App",
  components: {},
  data() {
    return {
      confettiWorker: "",
      countdown: 40,
    };
  },
  props: {
    event: Object,
  },
  async created() {
    this.countdown = this.getDaysTo();
    var myCanvas = document.createElement("canvas");
    document.body.appendChild(myCanvas);
    this.confettiWorker = confetti.create(myCanvas, { resize: true });

    this.confettiWorker();
  },
  methods: {
    getDaysTo() {
      const oneDay = 24 * 60 * 60 * 1000; // hours*minutes*seconds*milliseconds
      const firstDate = new Date();
      const secondDate = new Date(this.event.date);

      return Math.round(Math.abs((firstDate - secondDate) / oneDay));
    },

    async toggleStatus() {
      this.confettiWorker();
    },
  },
};
</script>

<style>
.event-name {
  position: absolute;
  top: 0;
  background-color: rgb(54, 17, 95);
  padding: 10px 20px;
  border-bottom-left-radius: 20px;
  border-bottom-right-radius: 20px;
  font-size: 20px;
  font-weight: bold;
}
#holderholder {
  display: flex;
  align-items: center;
  justify-content: center;
}
canvas {
  z-index: 30;
  position: absolute;
  top: 0;
  height: 100vh;
  width: 100vw;
  pointer-events: none;
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
  font-size: 5vh;
  padding: 0px 40px !important;
  line-height: 0.8;
  text-align: center;
  font-family: "AlmoniRegular";
  /* margin-top: 2vh !important; */
}

#holder {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 25vh;
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
}
</style>

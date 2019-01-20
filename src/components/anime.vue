<template>
  <div class="animation-container">
    <button @click="animateWaves">waverino</button>
    <div class="wave four">
      <SvgLoader svg="wave-four"/>
      <div class="fill-spacer"></div>
      <div class="fill"></div>
    </div>
    <div class="wave four extra-wave">
      <SvgLoader svg="wave-four"/>
      <div class="fill-spacer"></div>
      <div class="fill"></div>
    </div>
    <div class="wave three">
      <SvgLoader svg="wave-one"/>
      <div class="fill-spacer"></div>
      <div class="fill"></div>
    </div>
    <div class="wave three extra-wave">
      <SvgLoader svg="wave-one"/>
      <div class="fill-spacer"></div>
      <div class="fill"></div>
    </div>
    <div class="wave two">
      <SvgLoader svg="wave-one"/>
      <div class="fill-spacer"></div>
      <div class="fill"></div>
    </div>
    <div class="wave two extra-wave">
      <SvgLoader svg="wave-one"/>
      <div class="fill-spacer"></div>
      <div class="fill"></div>
    </div>
    <div class="wave one">
      <SvgLoader svg="wave-four"/>
      <div class="fill-spacer"></div>
      <div class="fill"></div>
    </div>
    <div class="wave one extra-wave">
      <SvgLoader svg="wave-four"/>
      <div class="fill-spacer"></div>
      <div class="fill"></div>
    </div>
    <!-- <div class="wave one"></div> -->
    <!-- <div class="animationcont">
        <svg class="one" viewBox="0 0 100 25">
          <path fill="#9EAFFD" opacity="0.5" d="M0 30 V15 Q30 3 60 15 V30z"></path>
          <path fill="#9EAFFD" d="M0 30 V12 Q30 17 55 12 T100 11 V30z"></path>
        </svg>
    </div>-->
  </div>
</template>

<script>
import SvgLoader from "@/components/SvgLoader";

export default {
  name: "anime",
  props: {
    msg: String
  },
  components: {
    SvgLoader
  },
  data: () => {
    return {
      width: 500
    };
  },
  methods: {
    animate() {
      console.log("Here");
      anime({
        targets: ".bar2",
        duration: 1500,
        // easing: 'easeInSine',
        elasticity: 400,
        width: this.width
      });
    },
    animateWaves() {
      this.waveOne();
      // anime({
      //   targets: ".wave",
      //   duration: 1500,
      //   // easing: 'easeInSine',
      //   elasticity: 400,
      //   width: this.width
      // });
    },
    waveOne() {
      anime({
        targets: ".two",
        translateX: "100%",
        duration: 7200,
        loop: true,
        easing: "linear"
      });
      anime({
        targets: ".one",
        translateX: "100%",
        duration: 8800,
        loop: true,
        easing: "linear"
      });
      anime({
        targets: ".three",
        translateX: "100%",
        duration: 6500,
        loop: true,
        easing: "linear"
      });
      anime({
        targets: ".four",
        translateX: "100%",
        duration: 8200,
        loop: true,
        easing: "linear"
      });
      anime({
        targets: ".wobble-s",
        translateY: "50px",
        direction: "alternate",
        duration: 8200,
        loop: true,
        easing: "linear"
      });
      anime({
        targets: ".wobble-m",
        translateY: "80px",
        direction: "alternate",
        duration: 8200,
        loop: true,
        easing: "linear"
      });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
$waveOneFill: #fff;
$waveTwoFill: #000;
$waveThreeFill: #2b4149;
$waveFourFill: #448dad;

@keyframes animate {
  from {
    background-position: 0 0;
  }
  to {
    background-position: -100vw 0;
  }
}

@keyframes slide {
  0% {
    transform: translate3d(0, 0, 0);
  }
  100% {
    transform: translate3d(-1692px, 0, 0);
  }
}
body {
  margin: 0;
}

.animation-container {
  overflow: hidden;
  height: 100vh;
  position: absolute;
  top: 0px;
  width: 100%;
  z-index: -1;
  background: #f1f1f1;
}

.bar {
  background: red;
  width: 50px;
  height: 50px;
  margin-bottom: 10px;
}

.wave {
  width: 100%;
  position: absolute;
  bottom: 0;
  display: flex;
  flex-direction: column;

  &.one {
    height: 35vh;
    path {
      fill: $waveOneFill;
      stroke: $waveOneFill;
    }

    .fill {
      background-color: $waveOneFill;
    }
    .fill-spacer {
      padding-bottom: 15.5%;
    }
  }
  &.two {
    height: 50vh;

    path {
      fill: $waveTwoFill;
      stroke: $waveTwoFill;
    }

    .fill {
      background-color: $waveTwoFill;
    }
  }
  &.extra-wave {
    left: calc(-100% + 1px);
  }

  &.three {
    height: 55vh;
    path {
      fill: $waveThreeFill;
      stroke: $waveThreeFill;
    }

    .fill {
      background-color: $waveThreeFill;
    }
  }
  &.four {
    height: 55vh;
    path {
      fill: $waveFourFill;
      stroke: $waveFourFill;
    }

    .fill {
      background-color: $waveFourFill;
    }
    .fill-spacer {
      padding-bottom: 15.5%;
    }
  }
}
.fill-spacer {
  width: 100%;
  padding-bottom: 18.7%;
  height: 0px;
}
.fill {
  background: #000;
  width: 100%;
  flex-grow: 1;
  // padding-bottom: 20%;
  height: auto;
}
.svg-wave {
  width: 100%;
  position: absolute;
  height: auto;
}

.wave-one {
}
</style>

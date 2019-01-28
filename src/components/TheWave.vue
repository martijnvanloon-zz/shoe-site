<template>
  <div class="animation-container">
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
  </div>
</template>

<script>
import SvgLoader from "@/components/SvgLoader";

export default {
  name: "TheWave",
  props: {},
  components: {
    SvgLoader
  },
  data: () => {
    return {};
  },
  mounted() {
    this.animateWaves();
  },
  methods: {
    animateWaves() {
      this.waveOne();
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
$waveOneFill: #f1f1f1;
$waveTwoFill: #000;
$waveThreeFill: #2b4149;
$waveFourFill: #448dad;

.animation-container {
  overflow: hidden;
  height: 100%;
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
    height: 45vh;
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
    height: 60vh;

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
    height: 65vh;
    path {
      fill: $waveThreeFill;
      stroke: $waveThreeFill;
    }

    .fill {
      background-color: $waveThreeFill;
    }
  }
  &.four {
    height: 65vh;
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
  height: auto;
}
.svg-wave {
  width: 100%;
  position: absolute;
  height: auto;
}
</style>

<template>
  <div class="about">
    <div class="top-column">
      <div class="logo-container">
        <img src="../assets/logo.png" alt class="logo">
      </div>
      <Navigation/>
      <Menu/>
    </div>
    <TheWave/>
    <div class="main-content">
      <div class="column-one">
        <Thumbnails/>
        <div class="price-container">
          <span class="label">Color:</span>
          <ColorRadio code="#538cab" name="Blue"/>
          <ColorRadio code="#64454e" name="Mauve"/>
        </div>
      </div>
      <div class="column-two">
        <div class="titles">
          <h1 class="h1">Yeezy 700</h1>
          <h2 class="h2">waverunners</h2>
        </div>

        <div class="visual">
          <img src="../assets/schoen-groot.png" alt>
          <img src="../assets/shadow-normal@3x.png" alt>
        </div>

        <div class="copy-container">
          <p
            class="main-copy"
          >Ride the wave! Adding another unique sneaker to his line Kanye West introduced the adidas Yeezy Boost 700 Wave Runner in 2017. An eye-catching look with a chunky sole and running inspired upper.</p>
        </div>
      </div>
      <div class="column-three">
        <aside class="ye">
          <figure>
            <img src="..\assets\7e3e1a13fb337f7d4cdb19fa028018e1.1000x1000x1.png" alt>
            <figcaption>Adidas Yeezy is the official collaboration with Kanye West</figcaption>
          </figure>
          <a href>Read more ></a>
        </aside>
        <select name="size" id="size">
          <option value>46</option>
          <option value>47</option>
          <option value>48</option>
          <option value>49</option>
        </select>
        <button>Purchase</button>
      </div>
    </div>
  </div>
</template>
<script>
import TheWave from "@/components/TheWave.vue";
import Navigation from "@/components/Navigation.vue";
import ColorRadio from "@/components/ColorRadio.vue";
import Thumbnails from "@/components/Thumbnails.vue";
import Menu from "@/components/Menu.vue";
// const anime = anime;
export default {
  name: "home",
  components: {
    TheWave,
    Navigation,
    ColorRadio,
    Thumbnails,
    Menu
  },
  data: () => {
    return {};
  },
  mounted() {
    this.enterVisual();
  },
  methods: {
    enterVisual() {
      anime({
        targets: ".visual",
        duration: 2500,
        translateY: "15px",
        easing: "easeInOutSine",
        direction: "alternate",
        loop: true
      });
    }
  }
};
</script>

<style lang="scss">
$font_path: "~@/assets/fonts/";
$font: "Tstar Regular", arial;
$font_bold: "Tstar Bold", arial;
$font_light: "Tstar Light", arial;

@font-face {
  font-family: "Tstar Light";
  src: url($font_path+"yeezy_tstar-light-webfont.ttf") format("truetype");
}
@font-face {
  font-family: "Tstar Regular";
  src: url($font_path+"yeezy_tstar-regular-webfont.ttf") format("truetype");
  font-weight: 600;
  font-style: normal;
}
@font-face {
  font-family: "Tstar Bold";
  src: url($font_path+"yeezy_tstar-bold-webfont.ttf") format("truetype");
  font-weight: 800;
}

html {
  font-size: 20px;
}
body {
  margin: 0;
}

#app {
  font-family: "Roboto Mono", monospace;
  font-weight: 400;
  position: relative;
  min-height: 100vh;
}

.top-column {
  display: flex;
  height: 150px;
}

.logo {
  height: 150px;
}

.menu {
  display: flex;
  margin-left: auto;

  img {
    width: 60px;
  }
}

.main-content {
  display: flex;
  max-width: 100vw;
  justify-content: space-between;
}

.column-two {
  width: 60%;
  flex-grow: 1;
}

.visual {
  img {
    width: 100%;
    max-width: 40vw;
    min-width: 300px;
  }
}

.titles {
  color: #000;

  h1 {
    font-family: $font_bold;
    font-size: 7.594em;
    margin-bottom: 0;
    margin-top: 0;
  }

  h2 {
    font-family: $font;
    font-size: 3.375em;
    margin-top: -1rem;
    letter-spacing: 0.5rem;
  }
}

.copy-container {
  max-width: 800px;
  margin: auto;
  text-align: left;
  line-height: 2;
  background: #f1f1f1;
}

.column-one,
.column-three,
.logo-container {
  width: 20%;
}

.logo-container {
  display: flex;
}

.image-picker,
.price-container,
.logo {
  margin-left: 5vw;
}

.column-one {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: space-between;
}

.ye {
  img {
    width: 200px;
  }
}

.thumbnail {
  width: 130px;
  height: 130px;
  border-radius: 50%;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  &:not(:last-child) {
    margin-bottom: 1rem;
  }

  img {
    width: 150px;
  }
}
</style>

<template>
  <div class="about">
    <anime/>
    <div class="top-column">
      <div class="logo-container">
        <img src="../assets/logo.png" alt class="logo">
      </div>
      <div class="nav">
        <ul>
          <li>Men</li>
          <li>Women</li>
          <li>Kids</li>
          <li>Accessories</li>
        </ul>
      </div>
      <div class="menu">
        <div class="logo">
          <img src="../assets/icon-shopping-27.jpg" alt srcset>
        </div>
        <div class="logo">
          <img src="../assets/icon-shopping-27.jpg" alt srcset>
        </div>
      </div>
    </div>
    <div class="main-content">
      <div class="column-one">
        <div class="thumb-container">
          <div class="thumbnail">
            <img src="../assets/schoen-groot.png" alt>
          </div>
          <div class="thumbnail">
            <img src="../assets/yeezy700-side-small.png" alt>
          </div>
          <div class="thumbnail">
            <img src="../assets/bottom-yeezy.png" alt>
          </div>
        </div>
        <div class="price-container">
          <span class="price">$300</span>
          <span class="option-lable">Color</span>
          <label for="blue">Blue</label>
          <input type="radio" name id="blue">
          <label for="mauve">Mauve</label>
          <input type="radio" name id="mauve">
        </div>
      </div>
      <div class="column-two">
        <h1 class="h1">Yeezy 700</h1>
        <h2 class="h2">waverunners</h2>
        <img src="../assets/schoen-groot.png" alt>
        <img src="../assets/shadow-normal@3x.png" alt>
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
      </div>
    </div>
  </div>
</template>
<script>
import anime from "@/components/anime.vue";
export default {
  name: "home",
  components: {
    anime
  }
};
</script>

<style lang="scss">
#app {
}
.top-column {
  display: flex;
  height: 150px;
}
.logo {
  height: 150px;
}
.nav {
  ul {
    display: flex;
  }
  li {
    list-style: none;
    display: block;
    width: 160px;
  }
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
}

.column-two {
  width: 70%;
}
.column-one {
  width: 15%;
}
.column-three {
  width: 15%;
}

.ye {
  img {
    width: 200px;
  }
}

.thumbnail {
  width: 100px;

  img {
    width: 150px;
  }
}
</style>


<template>
  <div :style="{ color: code }" class="label">
    <input checked class="radio" :id="name" type="radio" name="selector">
    <label class="radio-label" :for="name">{{name}}</label>
    <div class="check"></div>
  </div>
</template>

<script>
// import SvgLoader from "@/components/";

export default {
  name: "ColorRadio",
  props: {
    code: String,
    name: String
  },
  components: {},
  data: () => {
    return {};
  },
  methods: {}
};
</script>

<style lang="scss">
.price-container {
  display: flex;
  width: 100%;
  font-size: 1em;
}
.radio {
  position: absolute;
  visibility: hidden;
}
.radio-label {
  display: block;
  position: absolute;
  z-index: 9;
  order: 2;
  cursor: pointer;
  -webkit-transition: all 0.25s linear;
  padding-left: 1.8rem;
  color: #000;
}
.check {
  display: flex;
  order: 1;
  justify-content: center;
  align-content: center;
  position: relative;
  border: 1px solid #f1f1f1;
  border-radius: 100%;
  height: 25px;
  width: 25px;
  z-index: 5;
  transition: border 0.25s linear;
  -webkit-transition: border 0.25s linear;
}
.check::before {
  display: block;
  position: relative;
  content: "";
  border-radius: 100%;
  height: 17px;
  width: 17px;
  background: currentColor;
  margin: auto;
  transition: background 0.25s linear;
  -webkit-transition: background 0.25s linear;
}
input[type="radio"]:checked ~ .check {
  border: 1px solid currentColor;
}
input[type="radio"]:checked ~ .check::before {
  background: currentColor;
}

.label {
  align-items: center;
  display: flex;
  position: relative;

  &:not(:first-child) {
    margin-left: 1.2em;
    width: 80px;
  }
}
</style>

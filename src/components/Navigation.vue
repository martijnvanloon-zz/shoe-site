

<template>
  <div class="nav">
    <ul>
      <li>Men</li>
      <li>Women</li>
      <li>Kids</li>
      <li>Accessories</li>
    </ul>
  </div>
</template>

<script>
// import SvgLoader from "@/components/";

export default {
  name: "Navigation",
  props: {
    msg: String
  },
  components: {},
  data: () => {
    return {};
  },
  methods: {}
};
</script>

<style lang="scss">
.nav {
  font-family: "Roboto Mono", monospace;
  font-weight: 600;
  ul {
    display: flex;
  }
  li {
    list-style: none;
    display: block;
    width: 140px;
    text-align: left;
  }
}
</style>

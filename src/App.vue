<template>
  <div id="app">
    <Intro />
    <AboutUs />
  </div>
</template>

<script>
import Intro from "./components/Intro";
import AboutUs from "./components/AboutUs";
export default {
  name: "App",
  components: {
    Intro,
    AboutUs
  }
};
</script>

<style lang="scss">
body {
  margin: 0;
  padding: 0;
  background: #fafafa;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000;

  .container {
    width: 100%;
    max-width: 1460px;
    margin: 0 auto;
    padding: 0 15px;
  }
}
</style>

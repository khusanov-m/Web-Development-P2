<template>
  <section class="wrapper">
    <NavBar />
    <MainContent />
    <SideBar />
  </section>
</template>

<script>
import NavBar from "./components/layout/NavBar.vue";
import MainContent from "./components/layout/MainContent.vue";
import SideBar from "./components/layout/SideBar.vue";

export default {
  name: "App",
  components: {
    NavBar,
    MainContent,
    SideBar,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Lato:wght@400;500;700;900&display=swap");

:root {
  --primary-color-1: #110b56;
  --text-color-1: #0f3f62;
  --text-color-2: #79798b;
  --icon-color: #676e89;

  --dash-color-1: #8695a0;
  --dash-color-2: #2760F3;
  --dash-color-3: #54C1FB;
}

*,
*::after,
*::before {
  padding: 0;
  margin: 0;
  box-sizing: inherit;
}

html {
  // 1rem definition
  font-size: 62.5%; // 1 rem = 10px; 10px / 16px = 62.5%
  box-sizing: border-box;
  scroll-behavior: smooth;

  @media only screen and (max-width: 75em) {
    font-size: 56.25%; // 1 rem = 9px, 9/16 = 50%
  }

  @media only screen and (max-width: 68.75em) {
    font-size: 50%; // 1 rem = 8px, 8/16 = 50%
  }
}

body {
  box-sizing: border-box;
  font-family: "Lato", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100vh;
  position: relative;
}

.container {
  max-width: 144rem;
  margin: 0 auto;
}

.wrapper {
  display: flex;
}
</style>

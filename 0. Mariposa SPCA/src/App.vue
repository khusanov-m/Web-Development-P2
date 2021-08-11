<template>
  <section class="bg1">
    <TheHeader />
    <IntroInformation :title="'Keeping and Caring for Animals'" class="transform" />
    <TheAdopting />
  </section>

  <section class="bg2">
    <TheVolunteer />
    <IntroInformation :title="'Non-Profit focused on Protecting and Preserving'" :cred="true" class="pt-2" style="color: #fff" />
  </section>
</template>

<script>
import TheHeader from "./components/layout/TheHeader.vue";
import IntroInformation from "./components/IntroInformation.vue";
import TheAdopting from "./components/TheAdopting.vue";
import TheVolunteer from "./components/TheVolunteer.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    IntroInformation,
    TheAdopting,
    TheVolunteer,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap");

/*
MEDIA QUERY MANAGER

0 - 600px : Phone
600 - 900 px : Tablet portrait
900 - 1200 px : Tablet landscape
1200 - 1800 px : Normal style
1800 + : big desktop

$breakpoint argument choices:
- phone
- tab-port
- tab-land
- big-desktop

ORDER: Base + typography > general layout + grid > page layout > components

1em = 16px
*/

@mixin respond($breakpoint) {
  @if $breakpoint == huge-desktop {
    @media only screen and (max-width: 112.5em) {
      @content;
    } // 1800px
  }

  @if $breakpoint == big-desktop {
    @media only screen and (max-width: 106.25em) {
      @content;
    } // 1700px
  }

  @if $breakpoint == desktop {
    @media only screen and (max-width: 93.75em) {
      @content;
    } // 1500px
  }

  @if $breakpoint == mini-desktop {
    @media only screen and (max-width: 100em) {
      @content;
    } // 1400px
  }

  @if $breakpoint == tab-land {
    @media only screen and (max-width: 75em) {
      @content;
    } // 1200px
  }

  @if $breakpoint == tab-port {
    @media only screen and (max-width: 68.75em) {
      @content;
    } // 1100px
  }

  @if $breakpoint == tab-port-2 {
    @media only screen and (max-width: 56.25em) {
      @content;
    } // 900px
  }

  @if $breakpoint == tab-port-3 {
    @media only screen and (max-width: 50em) {
      @content;
    } // 800px
  }

  @if $breakpoint == mini-tab-port {
    @media only screen and (max-width: 43.75em) {
      @content;
    } // 700px
  }

  @if $breakpoint == big-phone {
    @media only screen and (max-width: 37.5em) {
      @content;
    } // 600px
  }

  @if $breakpoint == phone {
    @media only screen and (max-width: 31.25em) {
      @content;
    } // 500px
  }

  @if $breakpoint == min-phone {
    @media only screen and (max-width: 25em) {
      @content;
    } // 400px
  }
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

  @include respond(tab-land) {
    font-size: 56.25%; // 1 rem = 9px, 9/16 = 50%
  }

  @include respond(tab-port) {
    font-size: 50%; // 1 rem = 8px, 8/16 = 50%
  }

  overflow-x: hidden;
}

body {
  box-sizing: border-box;
  background-color: #000;
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000;
}

.container {
  max-width: 117rem;
  margin: 0 auto;
  position: relative;
}

.transform {
  transform: translateX(4rem);
}

.pt-2 {
  padding: 62.1rem 0 10rem;
}

.bg1 {
  background: linear-gradient(180deg, rgba(0, 0, 0, 0) 67.4%, #000000 100%),
    url("./assets/first-bg.png") no-repeat center center/cover;
  object-fit: cover;
}

.bg2 {
  background: linear-gradient(
      180deg,
      rgba(0, 0, 0, 0.7) 24.31%,
      rgba(0, 0, 0, 0) 73.48%
    ),
    linear-gradient(180deg, rgba(0, 0, 0, 0) 84.53%, #000000 100%),
    url("./assets/second-bg.png") no-repeat center center/cover;
  object-fit: cover;
}
</style>

<template>
  <section class="container" id="navbar">
    <div class="nav">
      <img src="../../assets/logo.svg" alt="logo" />
      <div>
        <h1>Medkit_</h1>
        <p>Dashboard v2.6.0</p>
      </div>
    </div>
    <the-navigation></the-navigation>
  </section>
</template>

<script>
import TheNavigation from "../content/TheNavigation.vue";

export default {
  components: {
    TheNavigation,
  },
};
</script>

<style lang="scss" scoped>
#navbar {
  position: fixed;
  width: 26.6rem;
  height: 100vh;
  background: #f5f6ff;
  padding-top: 4.2rem;
}

.nav {
  margin: 0 0 4rem 2.8rem;
  display: flex;
  align-items: center;

  img {
    width: 5rem;
    height: 5rem;
  }

  div {
    margin-left: 1.4rem;

    h1 {
      color: var(primary-color-1);
      font-weight: 900;
      font-size: 2rem;
      margin-bottom: 0.8rem;
    }
    p {
      color: #b1b1c9;
      font-weight: 40;
      font-size: 1.2rem;
    }
  }
}
</style>

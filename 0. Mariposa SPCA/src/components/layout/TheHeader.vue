<template>
  <header class="container">
    <p>Mariposa SPCA</p>

    <nav>
      <ul>
        <li v-for="navItem in nav" :key="navItem"><a :href="`#` + navItem">{{ navItem }}</a></li>
      </ul>

      <BaseButton :donate="'Donate'" :second="false" />
    </nav>
  </header>
</template>

<script>
import BaseButton from "../ui/BaseButton.vue";

export default {
  components: {
    BaseButton,
  },

  data() {
    return {
      nav: [
        "adoption",
        "events",
        "memberships",
        "voluteer",
        "success Stories",
        "blog",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
header {
  padding-top: 5.5rem;
}

.container {
  display: flex;
  justify-content: space-between;
}

nav {
  display: flex;
  align-items: center;
}

ul {
  list-style-type: none;
  display: flex;

  li {
    margin-right: 2.4rem;
    font-size: 1.4rem;
    font-weight: 400;
    
    &::first-letter {
      text-transform: uppercase;
    }
  }
}

a {
  text-decoration: none;
  color: #000;
}

p {
  font-family: inherit;
  font-size: 1.4rem;
  font-weight: 600;
}
</style>

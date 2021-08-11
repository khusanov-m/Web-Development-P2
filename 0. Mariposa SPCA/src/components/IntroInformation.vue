<template>
  <section class="container">
    <div>
      <h1
        :class="[
          title === 'Non-Profit focused on Protecting and Preserving'
            ? 'second-title'
            : '',
        ]"
      >
        {{ title }}
      </h1>
      <div class="text">
        <p>
          Mariposa SPCA is a non-profit working to keep and care for animals and
          enforcing laws relating to the cruelty of animals.
        </p>
        <p>
          The general purpose, for which this corporation is formed, is to
          provide an arena for local education and humane treatment to animals
          and to foster local interest in such a society.
        </p>
      </div>
    </div>
    <BaseButton :first="'Donate Now'" :second="'Learn More'" :cred="cred" />

    <p v-if="cred" class="cred">
      Built by <a href="https://khusanov-m-r.netlify.app/">Khusanov M.R.</a>
      Designed by
      <a
        href="https://dribbble.com/shots/5101621-Mariposa-SPCA-Dribbble-Design-Challenge"
      >
        Darío Figueroa.
      </a>
      Copyrighted © 2021
    </p>
  </section>
</template>

<script>
import BaseButton from "./ui/BaseButton.vue";

export default {
  components: {
    BaseButton,
  },
  props: ["title", "cred"],
};
</script>

<style lang="scss" scoped>
.container > div {
  padding-bottom: 4.6rem;
}

h1 {
  font-size: 7.2rem;
  max-width: 70rem;
  line-height: 86px;
  margin: 22.4rem 0 5.1rem;
}

.text p {
  font-weight: 500;
  font-size: 1.8rem;
  line-height: 32px;
  max-width: 64rem;

  &:first-child {
    margin-bottom: 3rem;
  }
}

.cred {
  margin-top: 22.2rem;
  font-weight: 40;
  font-size: 16px;
  color: rgba(255, 255, 255, 0.6);

  a {
    text-decoration: none;
    color: currentColor;
  }
}

.second-title {
  max-width: 100rem;
}

.thirdBtn {
  width: 14.2rem;
  height: 5.1rem;
  border: 2px solid rgba(253, 180, 97, 0.82);
  color: rgba(253, 180, 97, 0.82);
  background-color: transparent;
}
</style>

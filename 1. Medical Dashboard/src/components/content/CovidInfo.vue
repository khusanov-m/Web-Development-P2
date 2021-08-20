<template>
  <div>
    <h1>Covid-19 World</h1>
    <p>
      The coronavirus COVID-19 is affecting 219 countries
    </p>
    <base-button :title="'Check your information'"></base-button>
  </div>
</template>

<script>
import BaseButton from "../ui/BaseButton.vue";

export default {
  components: {
    BaseButton,
  },
};
</script>

<style lang="scss" scoped>
div {
  padding: 3.6rem 4.2rem;
  background: url("../../assets/bg.png") no-repeat center center/cover;
  width: 32.4rem;
  color: #fff;
  text-align: center;
  border-radius: 10px;

  h1 {
    font-weight: 700;
    font-size: 2.6rem;
    margin-bottom: 1.9rem;
  }

  p {
    font-weight: 400;
    font-size: 1.4rem;
    line-height: 20px;
    text-align: center;
    letter-spacing: 0.02em;
    margin-bottom: 3.7rem;
  }
}
</style>

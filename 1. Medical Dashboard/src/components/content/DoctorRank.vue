<template>
  <section class="rank-stage">
    <div class="profile">
      <div class="profile__photo"></div>
      <mini-els></mini-els>
    </div>
    <h3>Rs. Bertha Medika</h3>
    <p>Jl. Cisaat, Sukabumi</p>
    <div class="numbers">
      <span>
        <h2>120</h2>
        <p>Room</p>
      </span>
      <span>
        <h2>#2</h2>
        <p>Reputation</p>
      </span>
      <span>
        <h2>33+</h2>
        <p>Best Doctor</p>
      </span>
    </div>
  </section>
</template>

<script>
import MiniEls from "../ui/MiniElements.vue";

export default {
  components: {
    MiniEls,
  },
};
</script>

<style lang="scss" scoped>
.rank-stage {
  width: 32.9rem;
  border: 1px solid #f2f2fd;
  border-radius: 17.2632px;
  padding: 2.8rem 3.8rem;
  position: relative;
  margin: 2.9rem 0 0 2.1rem;
}

.profile {
  display: flex;

  &__photo {
    width: 10.4rem;
    height: 10.4rem;
    border-radius: 50%;
    background-color: var(--primary-color-1);
    margin: 0 auto 1.8rem 7.5rem;
    cursor: pointer;
  }
}

h3 {
  font-weight: 900;
  font-size: 1.8rem;
  text-align: center;
  color: var(--primary-color-1);
  margin-bottom: 1rem;

  & ~ p {
    text-align: center;
    color: var(--icon-color);
    font-weight: 400;
    font-size: 1.2rem;
    margin-bottom: 3.7em;
  }
}

.numbers {
  display: flex;
  justify-content: center;
  text-align: center;

  span {
    padding: 0.5rem 1.5rem;

    h2 {
      font-weight: 900;
      font-size: 2.1rem;
      margin-bottom: 0.5rem;
    }

    p {
      font-weight: 400;
      font-size: 1.2rem;
      color: var(--icon-color);
    }

    &:not(:last-child) {
      border-right: 1px dashed #dbdde6;
    }
  }
}
</style>

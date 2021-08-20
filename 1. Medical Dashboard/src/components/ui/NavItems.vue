<template>
  <li @click="toggleActive">
    <div :class="{ active: isActive }">
      <img :src="require('../../assets/' + navContentsData.icon)" alt="icon" />
      <p>{{ navContentsData.title }}</p>
    </div>
  </li>
</template>

<script>
export default {
  props: ["navContentsData", "isActive"],
  methods: {
    toggleActive() {
      this.$emit("onToggle");
    },
  },
};
</script>

<style lang="scss" scoped>
li {
  list-style-type: none;
  margin-bottom: 1.6rem;
  display: inline-block;

  &:hover {
    cursor: pointer;
  }

  div {
    display: flex;
    align-items: center;
    width: 233px;
    height: 47px;
    padding-left: 2.7rem;
    border-radius: 6px;

    img {
      margin-right: 2rem;
      color: var(--icon-color);
    }

    p {
      font-weight: 500;
      font-size: 1.4rem;
      color: #79798b;

      &:first-letter {
        text-transform: uppercase;
      }
    }
  }

  &:last-child {
    margin-top: 30.4rem;
  }
}

div.active {
  background: linear-gradient(
    90.25deg,
    rgba(71, 72, 111, 0.2) -23.64%,
    rgba(71, 72, 111, 0) 87.49%
  );
  color: #56549e;
  border: 1px solid #e7e9fe;

  img {
    color: var(--primary-color-1);
  }

  p {
    color: #56549e;
  }
}
</style>

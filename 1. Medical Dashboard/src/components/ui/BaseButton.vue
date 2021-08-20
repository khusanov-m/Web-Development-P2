<template>
  <button>{{ title }}</button>
</template>

<script>
export default {
  props: ["title"],
};
</script>

<style lang="scss" scoped>
button {
  width: 24rem;
  height: 4.6rem;
  background: #fff;
  border-radius: 6px;
  border: none;
  font-weight: 700;
  font-size: 1.4rem;
  font-family: inherit;
  display: inline-block;
  transition: .2s ease;

  &:hover {
    cursor: pointer;
  }

  &:active {
    transform: translateY(3px);
  }
}
</style>

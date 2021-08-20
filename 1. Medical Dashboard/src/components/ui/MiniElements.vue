<template>
  <div class="mini-els">
    <span></span>
    <span></span>
  </div>
</template>

<style lang="scss" scoped>
.mini-els {
  display: flex;
  cursor: pointer;

  transition: 0.2s ease;

  &:hover {
    cursor: pointer;
  }

  &:active {
    transform: translateY(3px);
  }

  span {
    width: 5px;
    height: 5px;
    background: #0f3f62;
    border-radius: 50%;

    &:first-child {
      margin-right: 1.4rem;
    }
  }
}
</style>

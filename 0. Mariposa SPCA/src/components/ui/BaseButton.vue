<template>
  <button class="donate" v-if="!!donate">{{ donate }}</button>
  <button class="firstBtn" v-if="!!first">{{ first }}</button>
  <button v-if="!!second" class="secondBtn" :class="[cred === true ? 'thirdBtn' : 'secondBtn']">
    {{ second }}
  </button>
</template>

<script>
export default {
  props: ["first", "second", "donate", "title", 'cred'],
};
</script>

<style lang="scss" scoped>
$primary-btn-color: rgba(253, 180, 97, 0.82);
$secondary-btn-color: rgba(62, 34, 3, 0.82);

.firstBtn,
.secondBtn {
  border-radius: 8px;
  cursor: pointer;
  color: $secondary-btn-color;
  font-weight: 600;
  font-size: 1.8rem;
  font-family: inherit;

  transition: 0.1s ease;

  &:active {
    transform: translateY(3px);
  }
}

.firstBtn {
  width: 15rem;
  height: 5.1rem;
  border: 0;
  background-color: $primary-btn-color;
  margin-right: 2.4rem;
}

.secondBtn {
  width: 14.2rem;
  height: 5.1rem;
  border: 2px solid $secondary-btn-color;
  background-color: transparent;
}

.donate {
  width: 7.2rem;
  height: 2.7rem;
  font-weight: 400;
  font-size: 1.4rem;
  font-family: inherit;
  background-color: $primary-btn-color;
  border: 0;
  border-radius: 4px;
  cursor: pointer;

  transition: 0.1s ease;

  &:active {
    transform: translateY(2px);
  }
}

.thirdBtn {
  border: 2px solid rgba(253, 180, 97, 0.82);
  color: rgba(253, 180, 97, 0.82);
}
</style>

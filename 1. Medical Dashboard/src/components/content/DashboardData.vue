<template>
  <main class="item">
    <div class="filter">
      <h3>Health Report Patient</h3>
      <div>
        <input type="month" name="Monthly" placeholder="Monthly" required />
        <img src="../../assets/calendar.svg" alt="calendar" class="calendar" />
      </div>
    </div>
    <GraphData />
  </main>
</template>

<script>
import GraphData from "./GraphData.vue";

export default {
  components: {
    GraphData,
  },
};
</script>

<style lang="scss" scoped>
.item {
  margin-top: 3.2rem;
  border: 1px solid #f2f2fd;
  border-radius: 2rem;
  padding: 2.4rem 4.4rem 2.6rem 2.6rem;
}

.filter {
  display: flex;
  align-items: center;
  justify-content: space-between;

  h3 {
    font-weight: 700;
    font-family: inherit;
    font-size: 1.6rem;
  }

  & > div {
    position: relative;
  }
}

input[type="month"] {
  position: relative;
  width: 17rem;
  height: 4rem;
  border: 0.5px solid #dbe5e5;
  border-radius: 4.5rem;
  padding: 0 1rem;
  font-size: 1.4rem;
  font-weight: 400;
  transition: width 0.3s linear;

  &:focus,
  &:active,
  &:valid {
    outline: none;
    width: 21rem;
  }

  &:valid {
    padding-left: 5rem;
    color: #0f3f62;

    &::after {
      right: 5%;
    }
  }

  &:focus + img,
  &:focus:valid + img,
  &:active:valid + img,
  &:valid + img {
    left: 13%;
  }

  &::-webkit-calendar-picker-indicator {
    color: transparent;
    background: none;
    z-index: 1;

    &:hover {
      cursor: pointer;
    }
  }

  &::after {
    font-family: "Font Awesome 5 Free";
    content: "\f078";
    position: absolute;
    font-weight: 900;
    top: 53%;
    right: 8%;
    transform: translate(-50%, -50%);
    color: #0f3f62;
  }

  &:invalid::before {
    content: attr(placeholder);
    color: var(--dash-color-1);
    width: 100%;
    padding-left: 4rem;
  }

  &:focus::before,
  &:active::before {
    content: "";
    width: 0%;
  }

  &:valid &::before,
  &:valid &::before {
    content: attr(value);
  }
}

img {
  position: absolute;
  transform: translate(-50%, -50%);
  top: 50%;
  left: 18%;
  z-index: 10;
  background: transparent;
}
</style>

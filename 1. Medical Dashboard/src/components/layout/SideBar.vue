// 22% длинна контента
<template>
  <section class="container" id="details">
    <div class="profile">
      <span></span>
      <i class="fas fa-chevron-down"></i>
    </div>
    <CovidInfo />
    <TheSchedule />
  </section>
</template>

<script>
import CovidInfo from "../content/CovidInfo.vue";
import TheSchedule from "../content/TheSchedule.vue";

export default {
  components: {
    TheSchedule,
    CovidInfo,
  },
};
</script>

<style lang="scss" scoped>
#details {
  margin-top: 4.7rem;
  position: fixed;
  right: 5rem;

  @media only screen and (max-width: 100em) {
    right: 1rem;
  }
}

.profile {
  display: inline-flex;
  align-items: center;
  justify-content: flex-end;
  width: 32.5em;
  margin: 0 0 5rem -2rem;

  span {
    width: 40px;
    height: 40px;
    background: var(--primary-color-1);
    border-radius: 50%;
    margin-right: 2.3rem;
    cursor: pointer;
  }

  i {
    color: #f68e5a;
    font-size: 1.5rem;

    &:hover {
      cursor: pointer;
    }
  }
}
</style>

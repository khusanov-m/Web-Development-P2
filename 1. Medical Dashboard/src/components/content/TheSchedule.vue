<template>
  <section class="schedule">
    <div class="details">
      <h2>Scheduled</h2>
      <a>View all</a>
    </div>

    <div class="items">
      <div class="item">
        <div>
          <h2>Medical Checkup</h2>
          <p>Tuesday, 11 Jan - 2021</p>
          <button>Healthy</button>
        </div>
        <div class="bullets">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>

      <div class="item">
        <div>
          <h2>Blood donors for humanity</h2>
          <p>Sunday 16 May - 2020</p>
          <button>Charity</button>
        </div>
        <div class="bullets">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
      <base-button class="btn" :title="'Check your Schedule'"></base-button>
    </div>
  </section>
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
.schedule {
  width: 32.5rem;
}

.details {
  display: flex;
  justify-content: space-between;
  margin: 6.2rem 0 3.2rem;
  align-items: center;

  h2 {
    color: var(--primary-color-1);
    margin-left: 2rem;
    font-size: 1.8rem;
    font-weight: 700;
  }

  a {
    text-decoration: none;
    color: #f68e5a;
    font-size: 1.2rem;
    font-weight: 400;

    &:hover {
      cursor: pointer;
    }
  }
}

.items {
  width: 32.4rem;
  background: #fcfcfc;
  box-shadow: 22px 22px 84px rgba(237, 238, 247, 0.7);
  border-radius: 10px;
  padding: 2.4rem 2.4rem 3.2rem;
}

.item {
  display: flex;
  color: var(--primary-color-1);
  justify-content: space-between;

  &:not(:last-of-type) {
    border-bottom: 1px solid #f7f7ff;
    padding-bottom: 2.4rem;
  }

  &:not(:first-child) {
    padding-top: 2.4rem;

    button {
      background: rgba($color: #67dfdf, $alpha: 0.1);
      color: #64d7d7;
    }
  }

  h2 {
    font-weight: 700;
    font-size: 1.6rem;
    margin-bottom: 0.8rem;
  }
  p {
    font-weight: 400;
    font-size: 1.2rem;
    color: #9090a4;
    margin-bottom: 2rem;
  }
  button {
    width: 10rem;
    height: 3rem;
    background: rgba($color: #f49f74, $alpha: 0.15);
    border-radius: 50px;
    border: none;
    color: #f49f74;
    font-family: inherit;
    font-weight: 400;
    font-size: 1.2rem;
    cursor: pointer;
  }

  .bullets {
    display: flex;
    justify-content: center;
    align-items: center;

    width: 36px;
    height: 36px;
    border-radius: 50%;
    background-color: rgba($color: #56549e, $alpha: 0.05);

    &:hover {
      cursor: pointer;
    }

    span {
      width: 3px;
      height: 3px;
      border-radius: 50%;
      background-color: #56549e;

      &:not(:last-child) {
        margin-right: 4px;
      }
    }
  }
}

.btn {
  background: url("../../assets/btn_bg.png") no-repeat center center/cover;
  color: #fff;
  font-family: inherit;
  font-weight: 700;
  font-size: 1.4rem;
  margin-top: 3.2em;
  width: 27.6rem;
}
</style>

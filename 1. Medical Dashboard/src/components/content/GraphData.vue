<template>
  <div class="table">
    <div class="text-wrap"><p class="text">Stability</p></div>
    <div class="numbers">
      <span>+100</span>
      <span>75</span>
      <span>50</span>
      <span>25</span>
      <span>0</span>
    </div>
    <div class="months">
      <span>Jan</span>
      <span>Feb</span>
      <span>Mar</span>
      <span>Apr</span>
      <span>May</span>
      <span>Jun</span>
      <span class="picked">Jul</span>
      <span>Aug</span>
      <span>Sep</span>
      <span>Oct</span>
      <span>Nov</span>
      <span>Dec</span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.table {
  position: relative;
  margin-top: 3.5rem;
}

.text {
  &-wrap {
    filter: drop-shadow(0px 4px 30px rgba(0, 0, 0, 0.05));
  }

  transform: translate(-50%, -17%);

  position: absolute;
  z-index: 100;
  left: 59.5%;

  width: 11.6rem;
  height: 4.5rem;
  background-color: #fff;
  clip-path: polygon(0 0, 100% 0, 100% 75%, 60% 75%, 50% 100%, 40% 75%, 0 75%);
  border-radius: 5px;

  color: #62d2ff;
  font-size: 1.4rem;
  font-weight: 400;
  text-align: center;
  padding-top: 0.7rem;
}

.numbers {
  span {
    color: var(--dash-color-1);
    font-size: 1.2rem;
    font-weight: 400;
    position: relative;
    display: flex;
    justify-content: flex-end;
    width: 3rem;

    &:not(:last-child) {
      margin-bottom: 3.2rem;
    }

    &::after {
      content: "";
      position: absolute;
      width: 71rem;
      height: 0.5px;
      background-color: #dbe5e5;
      transform: translate(7%, -50%);
      left: 0%;
      top: 50%;
      z-index: -1;
    }
  }
}

.months {
  margin: 1.8rem 0 0 8.6rem;
  display: inline-block;

  span {
    color: var(--dash-color-1);
    font-size: 1.2rem;
    font-weight: 400;
    position: relative;

    &:not(:last-child) {
      margin-right: 3.8rem;
    }

    &::before,
    &::after {
      content: "";
      position: absolute;
      transform: translate(-50%, -50%);
      width: 2.4rem;
    }

    &::before {
      background-color: var(--dash-color-3);
      border-top-left-radius: 5px;
      border-top-right-radius: 5px;
    }

    &::after {
      background-color: var(--dash-color-2);
      border-bottom-left-radius: 5px;
      border-bottom-right-radius: 5px;
    }

    &:nth-child(2) {
      &::before {
        top: -15.7rem;
        height: 7.7rem;
        left: 50%;
      }
      &::after {
        top: -10.8rem;
        height: 2.1rem;
        left: 50%;
      }
    }
    &:nth-child(3) {
      &::before {
        top: -13rem;
        height: 2.4rem;
        left: 50%;
      }
      &::after {
        top: -8.8rem;
        height: 6rem;
        left: 50%;
      }
    }
    &:nth-child(4) {
      &::before {
        top: -14.6rem;
        height: 5.4rem;
        left: 50%;
      }
      &::after {
        top: -9.8rem;
        height: 4.2rem;
        left: 50%;
      }
    }
    &:nth-child(5) {
      &::before {
        top: -15.4rem;
        height: 7rem;
        left: 50%;
      }
      &::after {
        top: -8.1rem;
        height: 7.6rem;
        left: 50%;
      }
    }
    &:nth-child(6) {
      &::before {
        top: -13.7rem;
        height: 3.6rem;
        left: 50%;
      }
      &::after {
        top: -8.9rem;
        height: 6rem;
        left: 50%;
      }
    }
    &:nth-child(7) {
      &::before {
        top: -14.5rem;
        height: 5.4rem;
        left: 50%;
      }
      &::after {
        top: -10.8rem;
        height: 2.1rem;
        left: 50%;
      }
    }
    &:nth-child(8) {
      &::before {
        top: -13rem;
        height: 2.4rem;
        left: 50%;
      }
      &::after {
        top: -10.3rem;
        height: 3.1rem;
        left: 50%;
      }
    }
    &:nth-child(9) {
      &::before {
        top: -15.3rem;
        height: 7rem;
        left: 50%;
      }
      &::after {
        top: -8.5rem;
        height: 6.7rem;
        left: 50%;
      }
    }

    &:nth-child(11) {
      &::before {
        top: -16rem;
        height: 8.4rem;
        left: 50%;
      }
      &::after {
        top: -10.3rem;
        height: 3.1rem;
        left: 50%;
      }
    }
    &:nth-child(12) {
      &::before {
        top: -14.2rem;
        height: 4.6rem;
        left: 50%;
      }
      &::after {
        top: -9.6rem;
        height: 4.6rem;
        left: 50%;
      }
    }

    &:nth-child(1),
    &:nth-child(10) {
      &::before {
        top: -14.8rem;
        left: 50%;
        height: 6rem;
      }
      &::after {
        top: -9.5rem;
        left: 50%;
        height: 4.6rem;
      }
    }

    &.picked {
      color: #0e1566;
    }
  }
}
</style>

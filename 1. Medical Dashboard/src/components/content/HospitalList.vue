<template>
  <section class="recommends">
    <div class="title">
      <h3>Recommended Hospital</h3>
      <mini-els></mini-els>
    </div>
    <ul class="hospitals">
      <li class="hospital" v-for="hospital in hospitals" :key="hospital">
        <img src="../../assets/plane.svg" alt="plane" />
        <span>
          <h4>{{ hospital.name }}</h4>
          <p>{{ hospital.owner }}</p>
        </span>
        <i class="fas fa-arrow-right"></i>
      </li>
    </ul>
  </section>
</template>

<script>
import MiniEls from "../ui/MiniElements.vue";

export default {
  components: {
    MiniEls,
  },
  data() {
    return {
      hospitals: [
        { name: "Rs. Hasan Sadikin", owner: "Jl. Pasteur ,Bandung" },
        { name: "Rs. Assyfa Sukabumi", owner: "Jl. Jendral Sudirman,Sukabumi" },
        { name: "Rs. Kartika Kasih", owner: "Jl. Ahmad Yani, Sukabumi" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.recommends {
  margin-top: 3.2rem;
  width: 36.4rem;
  height: fit-content;
  background: #fff;
  border: 1px solid #f2f2fd;
  box-shadow: 0px 21.6667px 43.3333px rgba(48, 77, 96, 0.03);
  border-radius: 16.25px;
  padding: 3rem 2.6rem 2.1rem;

  i, img {
    cursor: pointer;

  }
}

.hospitals {
  list-style-type: none;
  margin-top: 2.6rem;
}

.hospital {
  display: flex;
  align-items: center;

  &:not(:last-child) {
    border-bottom: 0.541667px solid #dbe6e6;
    margin-bottom: 2.4rem;
    padding-bottom: 2.4rem;
  }

  img {
    margin-right: 1.8rem;
  }

  span {
    h4 {
      font-weight: 700;
      font-family: inherit;
      font-size: 1.5rem;
      color: #0f3f62;
      margin-bottom: 0.5rem;
    }

    p {
      font-weight: 400;
      font-size: 1.3rem;
      color: #8695a0;
    }
  }

  i {
    margin-left: auto;
    font-size: 1.2rem;
  }
}

.title {
  display: flex;
  align-items: center;
  justify-content: space-between;

  h3 {
    font-family: inherit;
    font-weight: 700;
    font-size: 1.7rem;
  }
}
</style>

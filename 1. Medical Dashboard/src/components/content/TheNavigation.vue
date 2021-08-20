<template>
  <ul class="navItems">
    <nav-items
      v-for="(navContent, index) in navContents"
      :key="index"
      :navContentsData="navContent"
      :isActive="activeIndex === index"
      @onToggle="onToggle(index)"
    >
    </nav-items>
  </ul>
</template>

<script>
import NavItems from "../ui/NavItems.vue";
export default {
  components: { NavItems },
  data() {
    return {
      navContents: [
        { title: "home", icon: "home.svg" },
        { title: "patient", icon: "profile.svg" },
        { title: "places", icon: "place.svg" },
        { title: "data & Notes", icon: "notes.svg" },
        { title: "Analytics", icon: "statistic.svg" },
        { title: "Setting", icon: "gear.svg" },
        { title: "log Out", icon: "out.svg" },
      ],
      activeIndex: null,
    };
  },
  methods: {
    onToggle(index) {
      if (this.activeIndex === index) {
        this.activeIndex = null;
      } else {
        this.activeIndex = index;
      }
    },
  },
  mounted: function() {
    this.activeIndex = 0;
  },
};
</script>

<style lang="scss" scoped>
.navItems {
  margin-left: 1.6rem;
}
</style>

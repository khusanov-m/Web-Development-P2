// 59.5% размер контента
<template>
  <section class="container" id="content">
    <TheHeader />
    <DashboardData />
    <div class="wrapper">
      <HospitalList />
      <DoctorRank />
    </div>
  </section>
</template>

<script>
import TheHeader from "../ui/TheHeader.vue";
import DashboardData from "../content/DashboardData.vue";
import HospitalList from "../content/HospitalList.vue";
import DoctorRank from "../content/DoctorRank.vue";

export default {
  components: {
    TheHeader,
    DashboardData,
    HospitalList,
    DoctorRank,
  },
};
</script>

<style lang="scss" scoped>
#content {
  width: fit-content;
  margin-top: 5.2rem;
  position: relative;

  @media only screen and (max-width: 100em) {
    left: -3.5rem;
  }
}

.wrapper {
  justify-content: center;
}
</style>

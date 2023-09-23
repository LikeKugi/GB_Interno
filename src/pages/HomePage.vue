<template>
  <div class="home">
    <HeroSection />
    <FollowProjects />
  </div>
</template>

<script>
import HeroSection from "@components/HeroSection.vue";
import FollowProjects from "@components/FollowProjects.vue";

export default {
  name: "HomePage",
  components: {FollowProjects, HeroSection}
};
</script>

<style scoped>

</style>

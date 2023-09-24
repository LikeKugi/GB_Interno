<script>
import PageHeader from "@components/PageHeader.vue";
import logo from '@assets/img/HeaderBackgrounds/ProjectDetails.png'

export default {
  name: "ProjectDetailsPage",
  data() {
    return {
      image: logo,
    }
  },
  components: {PageHeader}
};
</script>

<template>
  <div>
  <PageHeader :image="image"/>
</div>
</template>

<style scoped>

</style>

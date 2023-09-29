<script>
import headerImg from "@assets/img/HeaderBackgrounds/BlogDetails.png";
import PageHeader from "@components/PageHeader.vue";

export default {
  name: "BlogDetailsPage",
  components: {PageHeader},
  data() {
    return {
      headerImage: headerImg,
    };
  }
};
</script>


<template>
  <div>
    <PageHeader :image="headerImage"/>

  </div>
</template>

<style scoped lang="scss">

</style>

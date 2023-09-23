<script>
import ProjectsList from "@components/ProjectsList.vue";

export default {
  name: "FollowProjects",
  components: {ProjectsList},
  data() {
    return {
      projects: [
        {
          img: 'src/assets/img/projects/Image1.png',
          title: 'Modern Kitchan',
          text: 'Decor / Artchitecture',
          id: '1'
        },
        {
          img: 'src/assets/img/projects/Image2.png',
          title: 'Modern Kitchan',
          text: 'Decor / Artchitecture',
          id: '2'
        },
        {
          img: 'src/assets/img/projects/Image3.png',
          title: 'Modern Kitchan',
          text: 'Decor / Artchitecture',
          id: '3'
        },
        {
          img: 'src/assets/img/projects/Image4.png',
          title: 'Modern Kitchan',
          text: 'Decor / Artchitecture',
          id: '4'
        }
      ],
    }
  }
};
</script>

<template>
  <section class="projects">
    <div class="projects__container">
      <h2 class="projects__title">Follow Our Projects</h2>
      <p class="projects__text">It is a long established fact that a reader will be distracted by the of readable
        content of page lookings at its layouts points.</p>

      <ProjectsList :projects="projects"/>

    </div>
  </section>

</template>


<style scoped lang="scss">
@import "@styles/_index.scss";
.projects {
  @extend %section;

  &__container {
    @extend %container;
  }
  &__title {
    @extend %heading1;
    color: $primary2;
    text-align: center;
    margin-bottom: 10px;
  }
  &__text {
    margin: 0 auto;
    max-width: 740px;
    @extend %paragraphLarge;
    color: $secondary1;
    text-align: center;
    margin-bottom: 93px;
  }
}
</style>

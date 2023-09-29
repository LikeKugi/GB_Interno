<script>
import ProjectsCard from "@components/ProjectsCard.vue";

export default {
  name: "ProjectsList",
  components: {ProjectsCard},
  props: {
    projects: Array,
  },
  computed: {
    leftRow() {
      return this.projects.filter((_, idx) => !(idx % 2));
    },
    rightRow() {
      return this.projects.filter((_, idx) => idx % 2);
    }
  }
};
</script>

<template>
  <div class="projects">
    <div class="projects__column">
      <ProjectsCard v-for="project in leftRow"
                    :img="project.img"
                    :text="project.text"
                    :title="project.title"
                    :key="project.id"
                    :id="project.id"/>
    </div>
    <div class="projects__column">
      <ProjectsCard v-for="project in rightRow"
                    :img="project.img"
                    :text="project.text"
                    :title="project.title"
                    :key="project.id"
                    :id="project.id"/>
    </div>

  </div>
</template>

<style scoped
       lang="scss">
.projects {
  display: flex;
  flex-wrap: wrap;
  gap: 100px;

  &__column {
    display: flex;
    flex-direction: column;
    gap: 55px;
  }
}
</style>

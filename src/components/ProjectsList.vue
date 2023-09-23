<script>
import ProjectsCard from "@components/ProjectsCard.vue";

export default {
  name: "ProjectsList",
  components: {ProjectsCard},
  props: {
    projects: Array,
  }
};
</script>

<template>
  <div class="projects">
    <ProjectsCard v-for="project in projects"
                  :img="project.img"
                  :text="project.text"
                  :title="project.title"
                  :key="project.id"
                  :id="project.id"/>
  </div>
</template>

<style scoped>
.projects {
  display: flex;
  flex-wrap: wrap;
  gap: 55px 100px;
}
</style>

<script>
import ArticlesCard from "@components/ArticlesCard.vue";

export default {
  name: "ArticlesList",
  components: {ArticlesCard},
  props: {
    articles: Array,
  }
};
</script>

<template>
  <div class="cards">

    <ArticlesCard v-for="article in articles"
                  :id="article.id"
                  :title="article.title"
                  :img="article.img"
                  :date="article.date"
                  :tag="article.tag"
                  :key="article.id"/>

  </div>
</template>


<style scoped lang="scss">
.cards {
  display: flex;
  justify-content: space-between;
}
</style>

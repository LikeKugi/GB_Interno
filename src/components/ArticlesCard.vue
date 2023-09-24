<script>
import {router} from "@routes/routes.js";

export default {
  name: "ArticlesCard",
  props: {
    img: String,
    tag: String,
    title: String,
    date: String,
    id: Number
  },
  methods: {
    navigate() {
      router.push({path: `/blog/${this.id}`});
    }
  }
};
</script>

<template>
  <div class="card">
    <div class="card__image">
      <img :src="img"
           :alt="tag">
      <button class="card__btn-img">{{ tag }}</button>
    </div>
    <div class="card__description">
      <h3 class="card__title">{{ title }}</h3>
      <div class="card__actions">
        <p class="card__text">{{ date }} </p>
        <button class="card__btn-nav"
                @click="navigate">
          <svg xmlns="http://www.w3.org/2000/svg"
               width="52"
               height="53"
               viewBox="0 0 52 53"
               fill="none">
            <path d="M23.7714 32.9527L29.7143 26.267L23.7714 19.5813"
                  stroke="#292F36"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"/>
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>


<style scoped lang="scss">
@import "@styles/_index.scss";

.card {
  max-width: 382px;
  padding: 21px;
  border-radius: 62px;
  border: 1px solid #E7E7E7;
  box-shadow: 0 10px 30px 0 rgba(255, 255, 255, 0.25);
  transition: color 0.3s ease-in-out, background-color 0.3s ease-in-out;
  &__title {
    @extend %heading3;
    color: $primary2;
  }
  &__text {
    @extend %paragraphXs;
    color: $secondary1;
  }
  &__actions {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  &__btn {
    &-nav {
      background-color: $primary3;
      border-radius: 50%;
      border: none;
      outline: none;
      cursor: pointer;
      transition: all 0.3s ease-in-out;
    }
    &-img {
      position: absolute;
      bottom: 20px;
      left: 20px;
      display: block;
      padding: 4px 5px 8px 11px;
      border-radius: 8px 8px 8px 0;
      border-color: transparent;
      outline: none;
      background: #FFF;
      color: $secondary1;
      font-size: 16px;
      line-height: 150%;
      cursor: pointer;
      transition: color 0.3s ease-in-out, background-color 0.3s ease-in-out;
    }
  }
  &__image {
    position: relative;
  }
  &:hover {
    background-color: $primary3;
    .card__btn-nav {
      background-color: #fff;
    }
  }
}
</style>

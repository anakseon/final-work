<template>
   <section class="blog center">
      <h2 class="blog__title">Статьи & Новости</h2>
      <p class="blog__text">Хорошо известно, что читатель будет отвлекаться на читабельный контент страницы</p>
      <ArticlesComponent :quantity="3"></ArticlesComponent>
   </section>
</template>

<script>
import ArticlesComponent from '../../ArticlesComponent.vue'
export default {
  name: 'HomePageArticles',
  components: {
    ArticlesComponent
  },

  data () {
    return {

    }
  },

  mounted () {

  },

  methods: {

  }
}
</script>

<style lang="scss" scoped>
@import "../../../scss/vars";
.blog {
   margin-top: 96px;
   margin-bottom: 96px;
   &__title {
      margin-bottom: 12px;
      color: #292f36;
      text-align: center;
      font-family: $familyTitle;
      font-size: 50px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
      letter-spacing: 1px;
   }
   &__text {
      padding-left: calc(($widthSite - 811px) / 2);
      padding-right: calc(($widthSite - 811px) / 2);
      margin-bottom: 52px;
      color: #4d5053;
      text-align: center;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
   }
}
</style>

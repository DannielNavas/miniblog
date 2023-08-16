<template>
    <div class="container">
    <AboutMe />
    <div class="content">
      <main>
        <ArticleCard
          v-for="article in articles"
          :key="article.slug"
          :v-bind="articles"
        />
      </main>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
      return {
        articles: [
          {
            title: 'Mi primer post',
            slug: 'mi-primer-post',
            date: new Date(),
          }
        ]
      };
  },
  async mounted() {
    const url = 'https://beamish-biscochitos-1a5924.netlify.app/.netlify/functions/articles';
    const { articles } = await this.$http.$get(url);
    this.articles = {
      ...articles.map((article) => ({
        title: article.title,
        slug: article.slug,
        date: article.published_at,
      })),
    };
    }
}
</script>

<style lang="scss">
.container {
  @apply m-auto;
}
.container .content {
  @apply flex flex-col justify-center items-center sm:p-2 md:p-4 lg:p-8 xl:p-16;
  main {
    @apply max-w-5xl grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6;
  }
}
</style>

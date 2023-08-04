<template>
  <div class="article-card">
    Article Card
  </div>
</template>

<style lang="scss" scoped>
.article-card {
  @apply block bg-white sm:border sm:rounded-lg p-4;
  h3 {
    @apply font-bold text-xl mb-2 mt-0;
  }
  div.author {
    @apply my-2;
    p {
      @apply m-0;
    }
    small {
      @apply italic;
    }
  }
  figure {
    img {
      @apply w-full;
    }
  }
  p {
    @apply my-4 font-serif;
  }
  div.actions {
    @apply flex gap-2;
    .btn {
      @apply w-full text-center border rounded-full px-8 py-2 bg-gray-200 hover:bg-gray-300;
    }
  }
}
</style>
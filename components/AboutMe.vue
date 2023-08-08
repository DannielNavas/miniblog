<template>
  <div class="about-me">About Me
    <h1>Mini Blog</h1>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facilis, perspiciatis! Reiciendis odit eligendi voluptatem ex, deleniti id facere voluptatibus blanditiis sunt iusto autem, molestiae impedit reprehenderit sed doloremque quisquam quis.</p>
  </div>
</template>

<style lang="scss" scoped>
.about-me {
  @apply w-full flex flex-col justify-center items-center px-4 py-16 bg-gray-200;
  h1 {
    @apply font-black text-4xl text-gray-900 pb-2;
  }
  p {
    @apply text-lg py-2;
  }
}
</style>

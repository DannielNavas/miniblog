<template>
  <div class="layout-default">
    <header>
      <menu>
        <NuxtLink class="brand" to="/">Daniel Navas</NuxtLink>
        <NuxtLink to="/about">Sobre mí</NuxtLink>
      </menu>
    </header>
    <Nuxt />
  </div>
</template>

<script>
export default {
  name: 'LayoutDefault',
}
</script>

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

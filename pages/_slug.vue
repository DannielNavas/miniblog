<template>
  <div>
    {{ $route.params.slug }}
  </div>
</template>
<!-- TODO: el parametro que llegue por url en la ruta /:slug se muestra esta pagina -->
<script>
export default {
  name: 'SlugPage',
}
</script>

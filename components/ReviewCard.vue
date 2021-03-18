<template>
  <div class="card max-w-sm bg-white shadow-xl rounded-xl text-gray-900 text-center p-5 m-2">
    <img :src="`_nuxt/static/images/testi/${reviewer.photo}`" class="w-20 mx-auto mb-3">
    <h1 style="font-size: 24px; font-style:italic; font-weight: bold;"> {{ reviewer.name }} </h1>
    <p>" {{ reviewer.review }} "</p>
  </div>
</template>

<script>
export default {
  props: {
    reviewer: {
      type: Object,
      default: {}
    }
  }
}
</script>

<style>
.card img {
  border-radius: 50%;
}

</style>
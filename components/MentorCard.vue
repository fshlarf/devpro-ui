<template>
  <div
    class="card max-w-sm bg-white shadow-2xl rounded-xl text-gray-900 text-center p-5 m-2"
  >
    <img
      :src="`/images/testi/${lecturer.photo}`"
      class="w-20 mx-auto mb-3 rounded-full"
    />
    <h1 style="font-size: 24px; font-style:italic; font-weight: bold;">
      {{ lecturer.name }}
    </h1>
    <p>" {{ lecturer.bio }} "</p>
  </div>
</template>

<script>
export default {
  props: {
    lecturer: {
      type: Object,
      default: {}
    }
  }
};
</script>

<style></style>

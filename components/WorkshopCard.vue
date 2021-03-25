<template>
  <div
    class="card max-w-sm bg-white shadow-2xl rounded-xl text-gray-900 text-center p-5 m-2"
  >
    <img
      :src="`/images/workshop/${course.poster}`"
      class="w-full mx-auto mb-3"
    />
    <h1 style="font-size: 24px; font-style:italic; font-weight: bold;">
      {{ course.name }}
    </h1>
    <p>" {{ course.preview }} "</p>
  </div>
</template>

<script>
export default {
  props: {
    course: {
      type: Object,
      default: {}
    }
  }
};
</script>

<style></style>

<template>
  <div class="w-full flex justify-center bg-white items-center mx-auto card-feature xl:max-w-sm md:max-w-xxl lg: text-gray-800 shadow-lg rounded-xl text-center p-2 md:p-5 m-2 md:flex md:text-left xl:text-center xl:block">
    <div class="max-w-md">
      <h1 style="font-size: 24px; font-weight: bold;"> {{ reviewer.name }} </h1>
      <p class="xl:mb-3"> {{ reviewer.review }} </p>
    </div>
    <img class="hidden md:block md:order-first md:mr-5 lg:mr-10" :src="`/images/feature/${reviewer.photo}`">
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

@media only screen and (max-width: 1024px) {
  .card-feature img {
    width: 20%;
    height: 100%;
  }
}


</style>
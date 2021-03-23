<template>
  <div class="flex justify-center bg-white items-center mx-auto card-feature text-gray-800 shadow-lg rounded-xl text-center p-2 m-2 md:max-w-xl md:p-5 md:text-left lg:text-center lg:block transform hover:scale-105 cursor-pointer">
    <div class="max-w-md">
      <h1 style="font-size: 24px; font-weight: bold;"> {{ reviewer.name }} </h1>
      <p class="xl:mb-3"> {{ reviewer.review }} </p>
    </div>
    <img class="hidden md:block md:order-first md:mr-5" :src="`/images/feature/${reviewer.photo}`">
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

@media only screen and (min-width: 1024px) {
  .card-feature {
    width: 32%;
  }
}

@media only screen and (max-width: 768px) {
  .card-feature img {
    width: 30%;
    height: 100%;
  }
}


</style>
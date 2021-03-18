<template>
  <div class="relative testimonial my-20 sm:h-100">
    <!-- <img src="~/static/images/testi/testi-bg2.jpg" alt="" class="w-full object-cover testi-bg">
    <div class="absolute z-10 top-0 opacity-70 dark-layer overflow-hidden w-full bg-black"></div> -->
    <div class="review z-20 w-full px-2 md:px-10 lg:px-10 xl:px-20 flex flex-wrap justify-center items-center">
      <ReviewCard 
        v-for="user in users"
        :key="user.id"
        :reviewer = "user"
      />
      <!-- <img src="~/static/images/testi/user-1.jpg" alt="">
      <img src="~/static/images/testi/user-2.jpg" alt="">
      <img src="~/static/images/testi/user-3.jpg" alt=""> -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          "id" : 1,
          "name" : "John Doe",
          "photo" : "user-1.jpg",
          "review" : "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          "id" : 2,
          "name" : "Jane Doe",
          "photo" : "user-2.jpg",
          "review" : "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          "id" : 3,
          "name" : "Josh Doe",
          "photo" : "user-3.jpg",
          "review" : "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        }
      ]
    }
  }
}
</script>

<style>

.testi-bg {
  height: 550px;
}

.dark-layer {
  height: 550px;
}

@media only screen and (max-width: 1024px) {
  .testi-bg {
    height: 670px;
  }
  .dark-layer {
    height: 670px;
  }
}

@media only screen and (max-width: 768px) {
  .testi-bg {
    height: 920px;
  }
  .dark-layer {
    height: 920px;
  }
}

@media only screen and (max-width: 576px) {
  .testi-bg {
    height: 1000px;
  }
  .dark-layer {
    height: 1000px;
  }
}

</style>
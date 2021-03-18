<template>
  <div class="relative testimonial my-20 sm:h-100">
    <div class="text-white text-center z-20 w-full justify-center items-center mx-auto">
      <h1 class="fit-title text-blues">Devpro Mentors</h1>
      <div class="primary-line primary mx-auto"></div>
    </div>
    <div class="review z-20 w-full px-2 md:px-10 lg:px-10 xl:px-20 flex flex-wrap justify-center items-center">
      <ReviewCard 
        v-for="user in users"
        :key="user.id"
        :reviewer = "user"
      />
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

.primary-line {
  width: 80px;
  height: 4px;
  margin-top: 0.6rem;
  margin-bottom: 1rem;
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
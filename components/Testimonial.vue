<template>
  <div class="relative testimonial my-10">
    <div class="text-white text-center w-full justify-center items-center mx-auto">
      <h1 class="testi-title text-blues">Devpro Mentors</h1>
      <div class="primary-line primary mx-auto"></div>
    </div>
    <div class="w-full px-2 flex flex-wrap justify-center items-center">
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

.testi-title {
  font-size: 36px;
  font-weight: bold;
}

.primary-line {
  width: 80px;
  height: 4px;
  margin-top: 0.6rem;
  margin-bottom: 1rem;
}

</style>
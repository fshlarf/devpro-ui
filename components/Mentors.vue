<template>
  <div class="relative py-10 bg-gray-100 md:py-20 xl:bg-white">
    <div class="absolute z-0 w-full hidden md:block xl:top-32">
      <div class="overflow-hidden">
        <img src="/images/banner2.svg" class="hidden xl:block object-cover h-full" style="height: 100%;"/>
      </div>
    </div>
    <div class="relative z-10 text-white text-center w-full justify-center items-center mx-auto">
      <h1 class="mentor-title text-test">Devpro Mentors</h1>
      <div class="primary-line bg-test mx-auto"></div>
    </div>
    <div class="relative z-10 w-full px-2 flex flex-wrap justify-center items-center">
      <MentorCard 
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

.mentor-title {
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
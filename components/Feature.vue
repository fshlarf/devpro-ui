<template>
  <div class="bg-gray-100 md:py-20">
    <div class="relative z-10 mb-10 xl:max-w-7xl xl:mx-auto">
      <div class="relative z-10 text-center w-full justify-center items-center">
        <h1 class="fitur-title text-test">Devpro Features</h1>
        <div class="primary-line bg-test mx-auto"></div>
      </div>
      <div class="relative z-10 px-2 justify-center items-center lg:flex">
        <FeatureCard 
          v-for="user in users"
          :key="user.id"
          :reviewer = "user"
        />
      </div>

    </div>
<!-- <button class="transition duration-500 ease-in-out bg-blue-600 hover:bg-red-600 transform hover:-translate-y-1 hover:scale-110 ..."> -->

  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          "id" : 1,
          "name" : "Berpengalaman",
          "photo" : "fitur-1.jpg",
          "review" : "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          "id" : 2,
          "name" : "Modern Development",
          "photo" : "fitur-2.jpg",
          "review" : "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          "id" : 3,
          "name" : "Menyesuaikan Dunia Kerja",
          "photo" : "fitur-3.jpg",
          "review" : "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit."
        }
      ]
    }
  }
}
</script>

<style>

.fitur-bg {
  height: 550px;
}

.fitur-layer {
  height: 550px;
}

.fitur-title {
  font-size: 36px;
  font-weight: bold;
}

.back-fit {
  background-color: #548ffd;
}

.primary-line {
  width: 80px;
  height: 4px;
  margin-top: 0.6rem;
  margin-bottom: 1rem;
}

@media only screen and (max-width: 1024px) {
  .fitur-bg {
    height: 640px;
  }
  .fitur-layer {
    height: 640px;
  }
}

@media only screen and (max-width: 768px) {
  .fitur-bg {
    height: 600px;
  }
  .fitur-layer {
    height: 600px;
  }
}

@media only screen and (max-width: 576px) {
  .fitur-bg {
    height: 530px;
  }
  .fitur-layer {
    height: 530px;
  }
}

</style>
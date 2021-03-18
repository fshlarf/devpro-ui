<template>
  <div class="relative mb-10 xl:max-w-7xl xl:mx-auto">
    <div class="relative z-10 text-center w-full justify-center items-center">
      <h1 class="fitur-title text-blues">Devpro Features</h1>
      <div class="primary-line primary mx-auto"></div>
    </div>
    <div class="relative z-10 px-2 justify-center items-center lg:flex">
      <FeatureCard 
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
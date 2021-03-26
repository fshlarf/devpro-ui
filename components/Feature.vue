<template>
  <div class="bg-gray-100 py-10 md:py-20">
    <div class="relative z-10 mb-10 xl:max-w-7xl xl:mx-auto">
      <div class="relative z-10 text-center w-full justify-center items-center">
        <h1 class="fitur-title text-test">Devpro Features</h1>
        <div class="primary-line bg-test mx-auto"></div>
      </div>
      <div class="relative z-10 px-2 justify-center items-center lg:flex">
        <FeatureCard
          v-for="feature in features"
          :key="feature.id"
          :fitur="feature"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          id: 1,
          name: "Berpengalaman",
          photo: "fitur-1.jpg",
          description:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          id: 2,
          name: "Modern Development",
          photo: "fitur-2.jpg",
          description:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          id: 3,
          name: "Menyesuaikan Dunia Kerja",
          photo: "fitur-3.jpg",
          description:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit."
        }
      ]
    };
  }
};
</script>

<style>
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
</style>

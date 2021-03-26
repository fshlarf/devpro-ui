<template>
  <div class="relative py-10 md:py-20 bg-workshop">
    <div
      class="relative z-10 text-white text-center w-full justify-center items-center mx-auto"
    >
      <h1 class="workshop-title text-white">Devpro Workshops</h1>
      <div class="primary-line bg-white mx-auto"></div>
    </div>
    <div
      class="relative z-10 w-full px-2 flex flex-wrap justify-center items-center"
    >
      <WorkshopCard
        v-for="workshop in workshops"
        :key="workshop.id"
        :course="workshop"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      workshops: [
        {
          id: 1,
          name: "Workshop 1",
          poster: "workshop1.png",
          preview:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          id: 2,
          name: "Workshop 2",
          poster: "workshop1.png",
          preview:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          id: 3,
          name: "Workshop 3",
          poster: "workshop1.png",
          preview:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          id: 4,
          name: "Workshop 4",
          poster: "workshop1.png",
          preview:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          id: 5,
          name: "Workshop 5",
          poster: "workshop1.png",
          preview:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          id: 6,
          name: "Workshop 6",
          poster: "workshop1.png",
          preview:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        },
        {
          id: 7,
          name: "Workshop 7",
          poster: "workshop1.png",
          preview:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, maiores."
        }
      ]
    };
  }
};
</script>

<style>
.workshop-title {
  font-size: 36px;
  font-weight: bold;
}

.bg-workshop {
  background-image: linear-gradient(to right, #c198f7, #005ad9);
}

.primary-line {
  width: 80px;
  height: 4px;
  margin-top: 0.6rem;
  margin-bottom: 1rem;
}
</style>

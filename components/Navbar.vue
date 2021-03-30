<template>
  <section class="mx-auto antialiased select-none">
    <div class="mx-auto max-w-9xl">
      <nav
        class="bg-nav relative z-50 h-16 bg-transparent"
        x-data="{ showMenu: false }"
      >
        <div
          class="container relative flex flex-wrap items-center justify-between h-16 mx-auto font-medium sm:px-4 md:px-2 lg:justify-center"
        >
          <nuxt-link
            class="navbar-brand ml-10 d-block align-center my-auto"
            to="/"
          >
            <img
              src="/images/devpro.png"
              width="100"
              height="100"
              alt="image not found"
              class="d-inline-block align-center"
            />
          </nuxt-link>
          <div
            class="-top-2 left-0 items-start w-full h-full p-4 text-sm bg-gray-900 bg-opacity-50 md:w-3/4 md:absolute lg:text-base md:h-auto md:bg-transparent md:p-0 md:relative md:flex"
            :class="{ 'flex fixed show': showMenu, hidden: !showMenu }"
          >
            <div
              class="flex-col pt-5 w-full h-auto overflow-hidden rounded-lg select-none bg-gray-800 md:rounded-none md:relative md:flex md:flex-row md:overflow-auto md:bg-transparent"
            >
              <div
                class="nav-dev flex flex-col items-start justify-center w-full text-center md:mt-0 md:flex-row md:items-center"
              >
                <a
                  class="inline-block cursor-pointer w-full px-6 py-2 mx-0 font-semibold text-left text-white md:w-auto md:px-0 md:mx-2 hover:text-gray-300 xl:mx-7 md:text-center"
                  @click="goToSection('benefit')"
                >
                  Benefit
                </a>
                <a
                  class="inline-block cursor-pointer w-full px-6 py-2 mx-0 font-semibold text-left text-white md:w-auto md:px-0 md:mx-2 hover:text-gray-300 xl:mx-7 md:text-center"
                  @click="goToSection('feature')"
                >
                  Fitur
                </a>
                <a
                  class="inline-block cursor-pointer w-full px-6 py-2 mx-0 font-semibold text-left text-white md:w-auto md:px-0 md:mx-2 hover:text-gray-300 xl:mx-7 md:text-center"
                  @click="goToSection('workshop')"
                >
                  Workshop
                </a>
                <a
                  class="inline-block cursor-pointer w-full px-6 py-2 mx-0 font-semibold text-left text-white md:w-auto md:px-0 md:mx-2 hover:text-gray-300 xl:mx-7 md:text-center"
                  @click="goToSection('tools')"
                >
                  Tools
                </a>
                <a
                  class="inline-block cursor-pointer w-full px-6 py-2 mx-0 font-semibold text-left text-white md:w-auto md:px-0 md:mx-2 hover:text-gray-300 xl:mx-7 md:text-center"
                  @click="goToSection('mentors')"
                >
                  Pengajar
                </a>
              </div>
              <div
                class="flex justify-center pt-4 md:items-center md:w-1/3 md:flex-row md:py-0"
              >
                <span
                  class="inline-flex w-100 shadow-sm md:rounded-full md:w-auto"
                >
                  <a
                    class="flex justify-center cursor-pointer px-60 py-3 text-md font-bold leading-4 text-black transition duration-150 ease-in-out bg-white md:px-3 md:w-auto md:rounded-full lg:px-10 btn-daftar"
                    @click="goToSection('register')"
                  >
                    Daftar
                  </a>
                </span>
              </div>
            </div>
          </div>
          <div
            @click="clickMenu"
            class="absolute right-5 flex flex-col items-center justify-center w-10 h-10 rounded-full cursor-pointer md:hidden hover:bg-gray-400"
          >
            <svg
              class="w-6 h-6 text-gray-100"
              v-show="!showMenu"
              fill="none"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              stroke="currentColor"
              x-cloak
            >
              <path d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
            <svg
              class="w-6 h-6 text-gray-700"
              v-show="showMenu"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
              x-cloak
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              ></path>
            </svg>
          </div>
        </div>
      </nav>
    </div>
  </section>
</template>

<script>
// import func from "vue-editor-bridge";
export default {
  data() {
    return {
      showMenu: false
    };
  },
  mounted() {
    this.scrollNavbar();
  },
  methods: {
    clickMenu() {
      this.showMenu = !this.showMenu;
      console.log(this.showMenu);
    },
    goToSection(section) {
      var elmnt = document.getElementById(section);
      elmnt.scrollIntoView(true);
    },
    scrollNavbar() {
      document.addEventListener("scroll", function() {
        const bgNav = document.querySelector(".bg-nav");
        bgNav.classList.remove("bg-transparent");
        bgNav.classList.add("bg-gray-800");

        if (window.pageYOffset === 0) {
          bgNav.classList.add("bg-transparent");
          bgNav.classList.remove("bg-gray-800");
        }
      });
    }
  }
};
</script>

<style>
.show {
  display: block;
}

.nav-dev a:hover {
  color: #c198f7;
}

.btn-daftar:hover {
  background-color: #c198f7;
}
</style>

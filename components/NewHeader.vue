<template>
  <section class="container-fluid mx-auto antialiased bg-black select-none">
    <div class="mx-auto max-w-9xl">
        <nav class="relative z-50 h-24" x-data="{ showMenu: false }">
            <div class="container relative flex flex-wrap items-center justify-between h-24 mx-auto font-medium lg:justify-center sm:px-4 md:px-2">
                <nuxt-link class="navbar-brand ml-10 d-block align-center my-auto" to="/">
                    <img
                        src="/images/devpro.png"
                        width="110"
                        height="110"
                        alt="image not found"
                        class="d-inline-block align-center"
                    />
                </nuxt-link>
                <div class="top-0 left-0 items-start w-full h-full p-4 text-sm bg-gray-900 bg-opacity-50 md:w-3/4 md:absolute lg:text-base md:h-auto md:bg-transparent md:p-0 md:relative md:flex" :class="{'flex fixed show': showMenu, 'hidden': !showMenu }">
                    <div class="flex-col pt-0 w-full h-auto overflow-hidden bg-gray-900 rounded-lg select-none md:bg-transparent md:rounded-none md:relative md:flex md:flex-row md:overflow-auto">
                        <div class="flex flex-col items-start justify-center w-full text-center md:mt-0 md:flex-row md:items-center lg">
                            <a href="#" class="inline-block w-full px-6 py-2 mx-0 font-medium text-left text-blues md:w-auto md:px-0 md:mx-2 xl:mx-7 md:text-center">Home</a>
                            <a href="#" class="inline-block w-full px-6 py-2 mx-0 font-medium text-left text-gray-200 md:w-auto md:px-0 md:mx-2 hover:text-indigo-600 xl:mx-7 md:text-center">Benefit</a>
                            <a href="#" class="inline-block w-full px-6 py-2 mx-0 font-medium text-left text-gray-200 md:w-auto md:px-0 md:mx-2 hover:text-indigo-600 xl:mx-7 md:text-center">Teknologi</a>
                            <a href="#" class="inline-block w-full px-6 py-2 mx-0 font-medium text-left text-gray-200 md:w-auto md:px-0 md:mx-2 hover:text-indigo-600 xl:mx-7 md:text-center">Kontak</a>
                        </div>
                        <div class="flex justify-center pt-4 md:items-center md:w-1/3 md:flex-row md:py-0">
                            <span class="inline-flex w-100 shadow-sm md:rounded-full md:w-auto">
                                <a href="#" class="flex justify-center px-60 py-3 text-md font-bold leading-4 text-black transition duration-150 ease-in-out bg-yellow-300 md:px-3 md:w-auto md:rounded-full lg:px-10 hover:text-blues hover:bg-white">Daftar</a>
                            </span>
                        </div>
                    </div>
                </div>
                <div @click="clickMenu" class="absolute right-5 flex flex-col items-center justify-center w-10 h-10 rounded-full cursor-pointer md:hidden hover:bg-gray-100">
                    <svg class="w-6 h-6 text-gray-500" v-show="!showMenu" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor" x-cloak>
                        <path d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                    <svg class="w-6 h-6 text-gray-700" v-show="showMenu" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" x-cloak>
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                </div>
            </div>
        </nav>
    </div>
        

    <div class="px-0 -mt-24 pt-40 pb-20 md:px-10 lg:pt-0 md:pb-0 bg-header">
      <div class="d-flex justify-between px-8 mx-auto xl:px-8 md:flex-row">
        <div class="flex flex-wrap items-center sm:-mx-3">
          <div class="w-full lg:w-2/3 md:px-3">
            <div class="space-y-6 d-flex align-items-center my-auto sm:max-w-md lg:max-w-full md:space-y-4 lg:space-y-8 xl:space-y-9 sm:pr-5 xl:py-40 md:mt-10">
              <h1 class="text-4xl text-left tracking-tight text-gray-900">
                <span class="text-white font-semibold xl:inline sm:text-5xl md:text-2xl lg:text-3xl xl:text-5xl">Mulai Karir Bersama</span><br>
                <span class="text-blues font-extrabold uppercase sm:text-5xl md:text-4xl lg:text-5xl xl:text-8xl">Devpro Center</span>
              </h1><hr>
              <p class="text-left text-gray-300 sm:max-w-md lg:text-xl md:max-w-3xl">
                Dapatkan skill dan pengalaman untuk memasuki dunia karir profesional dengan mengikuti Bootcamp, Training dan Workshop yang diadakan oleh Devpro Center
              </p>
              <!-- <div class="relative flex justify-center text-center sm:space-x-4">
                <a href="#_" class="flex w-100 px-6 py-3 mb-0 text-lg text-white primary transition duration-200 rounded-full sm:mb-0 hover:bg-black sm:px-auto">
                  Daftar Sekarang
                </a>
              </div> -->
            </div>
          </div>
          <div class="w-full lg:w-1/3 hidden hero lg:py-40">
            <!-- <div class="overflow-hidden shadow-xl"> -->
              <img src="~/static/images/hero-4.jpg" class="mt-10"/>
            <!-- </div> -->
          </div>
        </div>
      </div>
    </div>

   
  </section>
</template>

<script>
export default {
    data() {
        return {
            showMenu: false
        }
    },
    methods: {
        clickMenu() {
            this.showMenu = !this.showMenu
            console.log(this.showMenu);
        }
    }
}
</script>

<style>
.show {
    display: block;
}

.bg-header {
  background: -webkit-linear-gradient( #1b3152, black);
}

@media only screen and (min-width: 1024px) {
  .bg-header {
    height: 40rem;
  }
  .hero {
    height: 40rem;
    margin: 0 auto;
    display: block;
  }
}

</style>
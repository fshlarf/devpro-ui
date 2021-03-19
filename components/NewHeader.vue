<template>
  <section class="mx-auto antialiased select-none">
    <div class="mx-auto max-w-9xl">
        <nav class="relative z-50 h-16" x-data="{ showMenu: false }">
            <div class="container relative flex flex-wrap items-center justify-between h-16 mx-auto font-medium lg:justify-center sm:px-4 md:px-2">
                <nuxt-link class="navbar-brand ml-10 d-block align-center my-auto" to="/">
                    <img
                        src="/images/devpro2.png"
                        width="100"
                        height="100"
                        alt="image not found"
                        class="d-inline-block align-center"
                    />
                </nuxt-link>
                <div class="-top-2 left-0 items-start w-full h-full p-4 text-sm bg-gray-900 bg-opacity-50 md:w-3/4 md:absolute lg:text-base md:h-auto md:bg-transparent md:p-0 md:relative md:flex" :class="{'flex fixed show': showMenu, 'hidden': !showMenu }">
                    <div class="flex-col pt-5 w-full h-auto overflow-hidden back-def rounded-lg select-none md:bg-transparent md:rounded-none md:relative md:flex md:flex-row md:overflow-auto">
                        <div class="flex flex-col items-start justify-center w-full text-center md:mt-0 md:flex-row md:items-center">
                            <a href="#" class="inline-block w-full px-6 py-2 mx-0 font-medium text-left text-blues md:w-auto md:px-0 md:mx-2 xl:mx-7 md:text-center">Home</a>
                            <a href="#" class="inline-block w-full px-6 py-2 mx-0 font-medium text-left text-gray-800 md:w-auto md:px-0 md:mx-2 hover:text-indigo-600 xl:mx-7 md:text-center">Benefit</a>
                            <a href="#" class="inline-block w-full px-6 py-2 mx-0 font-medium text-left text-gray-800 md:w-auto md:px-0 md:mx-2 hover:text-indigo-600 xl:mx-7 md:text-center">Teknologi</a>
                            <a href="#" class="inline-block w-full px-6 py-2 mx-0 font-medium text-left text-gray-800 md:w-auto md:px-0 md:mx-2 hover:text-indigo-600 xl:mx-7 md:text-center">Kontak</a>
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
        

    <div class="relative flex flex-wrap justify-around md:mx-auto">
      <div class="relative z-10 w-full lg:w-1/2 my-10 px-8 md:max-w-2xl md:mt-40 md:mb-24 xl:mt-48 tracking-tight">
        <h1 class="text-gray-800 text-2xl lg:ml-1 font-semibold md:text-2xl lg:text-3xl xl:text-4xl">Mulai Karir Bersama</h1>
        <h1 class="text-black text-4xl font-extrabold uppercase mb-3 md:text-4xl lg:text-4xl xl:text-7xl">Devpro Center</h1>
        <p class="text-left text-lg lg:ml-1 text-gray-700 sm:max-w-md md:text-lg md:max-w-2xl">
          Dapatkan skill dan pengalaman untuk memasuki dunia karir profesional dengan mengikuti Bootcamp, Training dan Workshop yang diadakan oleh Devpro Center
        </p>
      </div>
      <div class="relative z-10 w-full hidden items-center lg:block lg:w-1/3 lg:-pl-20 lg:pt-32 lg:pb-36">
        <div class="overflow-hidden">
          <img src="/images/coding3.svg" class="rounded-xl" style="width: 100%"/>
        </div>
      </div>
    </div>

    <div class="absolute z-0 w-full hidden md:block md:-top-10 lg:-top-5 xl:top-20">
      <div class="overflow-hidden">
        <img src="/images/raw/yellow/8116d.png" class="object-cover w-full" style="width: 100%; height: 700px"/>
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
<template>
  <div class="relative my-20">
    <div class="box-border flex flex-col justify-center items-center content-center px-4 mx-auto md:flex-row md:mt-10 max-w-8xl lg:px-16">

        <!-- Image -->
        <div class="box-border relative w-full max-w-md px-4 mt-5 mb-4 -ml-5 text-center bg-no-repeat bg-contain border-solid md:pl-8 md:mt-0 md:max-w-none lg:mb-0 md:w-1/2 hidden md:block">
            <img src="~/static/images/register-2.svg" class="px-5 xl:pl-16 xl:pr-20 " style="height: 100%;"/>
        </div>

        <!-- Content -->
        <div class="box-border order-first w-full max-w-md text-blues border border-solid border-gray-400 md:w-1/2 xl:mr-40 md:order-none">
            <div class="flex flex-col items-start justify-start w-full h-full p-5 lg:py-12 xl:py-18 md:px-5">
                    <h4 class="w-full text-3xl font-bold text-left reg-title">Mendaftar</h4>
                    <div class="relative w-full mt-5 space-y-3">
                        <div class="relative">
                            <label class="font-medium text-gray-100">Nama</label>
                            <input type="text" class="block w-full px-4 py-4 mt-1 text-md placeholder-gray-500 focus:outline-none focus:ring-4 focus:ring-blue-600 focus:ring-opacity-0 border border-gray-400 bg-transparent" placeholder="Nama Lengkap..." />
                        </div>
                        <div class="relative">
                            <label class="font-medium text-gray-100">Email</label>
                            <input type="text" class="block w-full px-4 py-4 mt-1 text-md placeholder-gray-500 focus:outline-none focus:ring-4 focus:ring-blue-600 focus:ring-opacity-0 border border-gray-400 bg-transparent" placeholder="Alamat Email..." />
                        </div>
                        <div class="relative">
                            <label class="font-medium text-gray-100">Password</label>
                            <input type="text" class="block w-full px-4 py-4 mt-1 text-md placeholder-gray-500 focus:outline-none focus:ring-4 focus:ring-blue-600 focus:ring-opacity-0 border border-gray-400 bg-transparent" placeholder="Password..." />
                        </div>
                        <div class="relative">
                            <a href="#_" class="inline-block w-full px-5 py-4 mt-5 text-lg font-bold bg-gray-200 text-center text-black transition duration-200 hover:bg-gray-400 ease">Daftar</a>
                        </div>
                    </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

input {
    color: rgb(230, 230, 230);
}

</style>
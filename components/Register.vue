<template>
  <div class="relative mt-20 primary md:px-5">
    <div class="flex flex-col justify-around mx-auto max-w-9xl md:flex-row md:py-10 xl:justify-center">

        <!-- Image -->
        <div class="relative max-w-md hidden md:w-1/3 md:block xl:w-1/2 xl:mx-20">
            <img src="~/static/images/register-2.svg" style="height: 100%;"/>
        </div>

        <!-- Content -->
        <div class="order-first max-w-xl md:w-1/2 md:order-none xl:w-1/2 xl:mx-20">
            <div class="text-blues max-w-md bg-white mx-auto md:shadow-xl md:rounded-xl">
                <div class="flex flex-col items-start justify-start p-5 md:px-5 lg:py-12 xl:py-18">
                        <h4 class="text-3xl font-bold text-left reg-title">Mendaftar</h4>
                        <div class="relative w-full mt-5 space-y-3">
                            <div class="relative">
                                <label class="font-medium text-gray-700">Nama</label>
                                <input type="text" class="block w-full p-4 mt-1 text-md placeholder-gray-500 focus:outline-none focus:ring-opacity-0 border border-gray-400 rounded-xl" placeholder="Nama Lengkap..." />
                            </div>
                            <div class="relative">
                                <label class="font-medium text-gray-700">Nomor Handphone</label>
                                <input type="text" class="block w-full p-4 mt-1 text-md placeholder-gray-500 focus:outline-none focus:ring-opacity-0 border border-gray-400 rounded-xl" placeholder="+62..." />
                            </div>
                            <div class="relative">
                                <label class="font-medium text-gray-700">Email</label>
                                <input type="text" class="block w-full p-4 mt-1 text-md placeholder-gray-500 focus:outline-none focus:ring-opacity-0 border border-gray-400 rounded-xl" placeholder="Alamat Email..." />
                            </div>
                            <div class="relative">
                                <label class="font-medium text-gray-700">Password</label>
                                <input type="text" class="block w-full p-4 mt-1 text-md placeholder-gray-500 focus:outline-none focus:ring-opacity-0 border border-gray-400 rounded-xl" placeholder="Password..." />
                            </div>
                            <div class="relative">
                                <a href="#_" class="inline-block w-full p-5 mt-5 text-lg font-bold primary text-center text-black transition duration-200 hover:bg-black ease rounded-xl">Daftar</a>
                            </div>
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
    color: rgb(107, 107, 107);
}

.bg-register {
    background-color: black;
    /* background: -webkit-linear-gradient( #F5BE35, #F5BE35, #ffea00); */
}
</style>
<template>
  <div class="mx-auto px-6 absolute flex flex-col justify-center items-center h-screen w-full">
      <div class="flex flex-col justify-center items-center bg-green px-8 py-5 rounded-lg shadow-xl">
          <img class="h-20 pb-2" src="../assets/rickandmorty.png" alt="Rick and Morty">
          <form class="w-full flex flex-col space-y-2" action="">
              <p class="text-black">Episode :</p>
              <input class="rounded-full px-4 py-2" type="text">
              <p class="text-black">Episode :</p>
              <input class="rounded-full px-4 py-2" type="text">
              <p class="text-black">Episode :</p>
              <input class="rounded-full px-4 py-2" type="text">
          </form>
          <div class="flex flex-col justify-center items-center space-x-0 md:flex-row md:space-x-4">
            <router-link to="/" class="text-blue bg-black rounded-full mt-6 px-6 py-2 transition ease-in-out delay-200 hover:bg-blue hover:text-black duration-300"><i class="fas fa-search pr-3"></i>Search</router-link>
            <router-link to="/" class="text-black bg-blue rounded-full mt-6 px-6 py-2 transition ease-in-out delay-200 hover:bg-black hover:text-blue duration-300"><i class="fas fa-arrow-left pr-3"></i>Go back</router-link>
          </div>
          
      </div>  
  </div>
  
</template>

<script>
export default {
    name: 'Form'
}
</script>

<style>

</style>
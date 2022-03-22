<template>
  <div class="mx-auto px-6 absolute text-center flex flex-col justify-center items-center h-screen w-full space-y-4">
      <img class="flex w-2/6" src="../assets/rickandmorty.png" alt="Rick and Morty">
      <p class="text-white w-full md:w-1/2 text-lg">
          Rick and Morty is an American adult animated science fiction sitcom created by Justin Roiland and Dan Harmon for Cartoon Network's nighttime programming block, Adult Swim.
      </p>
      <router-link to="/form" class="text-blue bg-black rounded-full px-6 py-4 transition ease-in-out delay-200 hover:bg-blue hover:text-black duration-300"><i class="fas fa-search pr-3"></i>Search characters</router-link>
  </div>
</template>

<script>
export default {
    name: 'Home',
}
</script>

<style>

</style>
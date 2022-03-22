<template>
  <div class="mx-auto px-6 absolute flex flex-col justify-center items-center h-screen w-full">
      <div class="flex flex-col justify-center items-center bg-green px-8 py-5 rounded-lg shadow-2xl">
          <img class="h-20 pb-2" src="../assets/rickandmorty.png" alt="Rick and Morty">

            <form class="w-full flex flex-col justify-center" action="/list">
            <div class="overflow-y-auto h-56 pr-2 space-y-2">
              <p class="text-black">Name :</p>
              <input v-model="name" class="rounded-full px-4 py-2" type="text">
              <p class="text-black">Episode :</p>
              <input v-model="episode" class="rounded-full px-4 py-2" type="text">
              <p class="text-black">Location :</p>
              <input v-model="location" class="rounded-full px-4 py-2" type="text">
            </div>
            <div class="flex flex-col justify-center items-center space-x-0 md:flex-row md:space-x-4">
                <input type="submit" class="text-blue bg-black rounded-full mt-6 px-6 py-2 transition ease-in-out delay-200 hover:bg-blue hover:text-black duration-300 cursor-pointer" @click="search(character)" value="Search">
                <router-link to="/" class="text-black bg-blue rounded-full mt-6 px-6 py-2 transition ease-in-out delay-200 hover:bg-black hover:text-blue duration-300"><i class="fas fa-arrow-left pr-3"></i>Go back</router-link>
            </div>
         </form> 
      </div>  
  </div>
  
</template>

<script>
export default {
    name: 'Form',
    methods: {
        search(character){
            this.id = character.id;
            this.firstName = character.firstName;
            this.lastName = character.lastName;
            this.email = character.email;
        }
    }
}
</script>

<style scoped>
::-webkit-scrollbar {
    width: 5px;
  }
  
  ::-webkit-scrollbar-track {
    background: black; 
    border-radius: 10px;
  }
   
  ::-webkit-scrollbar-thumb {
    background: #00B0C8; 
    border-radius: 10px;
  }
</style>
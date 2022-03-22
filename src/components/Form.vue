<template>
  <div class="mx-auto px-6 absolute flex flex-col justify-center items-center h-screen w-full">
      <div class="flex flex-col justify-center items-center bg-green px-8 py-5 rounded-lg shadow-2xl">
          <img class="h-20 pb-2" src="../assets/rickandmorty.png" alt="Rick and Morty">

            <form class="w-full flex flex-col justify-center" action="/list" method="GET">
            <div class="overflow-y-auto h-56 pr-2 space-y-2">
              <p class="text-black">Name :</p>
              <input v-model="name" class="rounded-full px-4 py-2" type="text">
              <p class="text-black">Status :</p>
              <input v-model="status" class="rounded-full px-4 py-2" type="text">
              <p class="text-black">Type :</p>
              <input v-model="type" class="rounded-full px-4 py-2" type="text">
              <p class="text-black">Gender :</p>
              <input v-model="gender" class="rounded-full px-4 py-2" type="text">
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
            this.status = character.status;
            this.type = character.type;
            this.gender = character.gender;
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
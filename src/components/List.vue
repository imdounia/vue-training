<template>
  <div class="mx-auto px-6 absolute flex flex-col justify-center items-center h-screen w-full">
      <div class="flex flex-col justify-center items-center bg-green px-8 py-5 rounded-lg shadow-2xl">
          <h2 class="text-blue font-bold text-2xl pb-5">List of characters</h2>
                <p class="text-white" v-if="error">Something went wrong...</p>
                <p class="text-white" v-if="loading">Loading...</p>
                <p class="text-white" v-else v-for="character in result.characters.results" :key="character.id">
                    {{ character.name }}
                </p>
                <div></div>
          <div class="flex flex-col justify-center items-center space-x-0 md:flex-row md:space-x-4">
            <router-link to="/form" class="text-black bg-blue rounded-full mt-6 px-6 py-2 transition ease-in-out delay-200 hover:bg-black hover:text-blue duration-300"><i class="fas fa-arrow-left pr-3"></i>Go back</router-link>
          </div>
          
      </div>  
  </div>
</template>

<script>
import gql from 'graphql-tag'
import { useQuery } from '@vue/apollo-composable'

const CHARACTERS_QUERY = gql`
  query Characters {
    characters {
      results {
        id
        name
        image
      }
    }
  }
`
export default {
    name:'List',
    setup () {
    const { result, loading, error } = useQuery(CHARACTERS_QUERY);
    return {
      result,
      loading, 
      error
    }
  }
}
</script>

<style>

</style>
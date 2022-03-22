<template>
  <div class="relative h-screen">
    <img class="absolute w-full max-w-full h-screen object-cover object-top brightness-50" src="./assets/bg.jpg" alt="Rick and Morty">
    <Header/>
    <router-view></router-view>
  </div>
  <Footer/>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    Header,
    Footer
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');

::-webkit-scrollbar {
    width: 3px;
  }
  
  ::-webkit-scrollbar-track {
    background: black; 
  }
   
  ::-webkit-scrollbar-thumb {
    background: #00B0C8; 
  }
</style>
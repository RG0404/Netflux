<template>
  <Navbar 
    :logo="require('./assets/logo-netflux.png')" 
    :profile="require('./assets/photo-user.png')"
  />

  <HeroBanner/>

  <Slider :movies="movies"/>
  
</template>

<script>
import Navbar from "./components/Navbar.vue";
import HeroBanner from "./components/HeroBanner.vue"
import Slider from "./components/Slider";

export default {
  name: 'App',

  components: {
    Slider,
    Navbar,
    HeroBanner
  },

  methods: {
    async getMovieData() {
      try {
        let response = await fetch("https://imdb-api.com/en/API/Top250Movies/k_vsnmlp8s");
        this.movies = await response.json();
      } catch (error) {
        console.log(error);
      }
    }
  },

  data() {
    return {
      movies: [

      ]
    }
  },

  mounted() {
    this.getMovieData();
  }

}
</script>

<style>

* {
  margin: 0;
  padding: 0;
  text-decoration: none;
  font-family: Arial, Helvetica, sans-serif;
}

body {
  background-color: rgb(20, 20, 20);
}

</style>

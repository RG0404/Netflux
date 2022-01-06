<template>
  <Navbar 
    :logo="require('./assets/logo-netflux.png')" 
    :profile="require('./assets/photo-user.png')"
  />

  <HeroBanner/>

  <Slider :movies="movies"
          :series="series" />
  
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
        let response = await fetch("https://imdb-api.com/fr/API/Top250Movies/k_vsnmlp8s");
        let movies = await response.json();
        this.movies = movies.items;
      } catch (error) {
        console.log(error);
      }
    },

    async getTvData() {
      try {
        let response = await fetch("https://imdb-api.com/fr/API/Top250TVs/k_vsnmlp8s");
        let series = await response.json();
        this.series = series.items;
      } catch (error) {
        console.log(error);
      }
    }
  },

  data() {
    return {
      movies: [

      ],

      series: [

      ],
    }
  },

  mounted() {
    this.getMovieData();
    this.getTvData();
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

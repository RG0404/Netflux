<template>
  <Navbar 
    :logo="require('./assets/logo-netflux.png')" 
    :profile="require('./assets/photo-user.png')"
  />

  <HeroBanner/>

  <Slider :movies="movies"
          :series="series"
          :soon="soon"
          :popular="popular" />
  
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
        let response = await fetch("https://edu.maxence.space/imdb/topmovies.json");
        let movies = await response.json();
        this.movies = movies.items;
      } catch (error) {
        console.log(error);
      }
    },

    async getTvData() {
      try {
        let response = await fetch("https://edu.maxence.space/imdb/toptv.json");
        let series = await response.json();
        this.series = series.items;
      } catch (error) {
        console.log(error);
      }
    },

  async getComingSoonData() {
    try {
      let response = await fetch("https://edu.maxence.space/imdb/comingsoon.json");
      let soon = await response.json();
      this.soon = soon.items;
    } catch (error) {
      console.log(error);
    }
  },

  async getMostPopularData() {
    try {
      let response = await fetch("https://edu.maxence.space/imdb/mostpopular.json");
      let popular = await response.json();
      this.popular = popular.items;
    } catch (error) {
      console.log(error);
    }
  },
},



  data() {
    return {
      movies: [

      ],

      series: [

      ],

      soon: [

      ],

      popular: [

      ],
    }
  },

  mounted() {
    this.getMovieData();
    this.getTvData();
    this.getComingSoonData();
    this.getMostPopularData();

    console.log('toto');
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

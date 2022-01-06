<template>
  
  <Navbar 
    :logo="require('./assets/logo-netflux.png')" 
    :profile="require('./assets/photo-user.png')"
  />

  <HeroBanner/>

  <Slider/>
  
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

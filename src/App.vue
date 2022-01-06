<template>
  
  <Navbar :image= "require('./assets/logo-netflux.png')" />
  <Slider/>
  
</template>

<script>
import Navbar from "./components/Navbar.vue"
import Slider from "./components/Slider";

export default {
  name: 'App',
  components: {
    Slider,
    Navbar
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

</style>

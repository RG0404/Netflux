<template>
  
  <Navbar :image= "require('./assets/logo-netflux.png')" />
  
</template>

<script>
import Navbar from "./components/Navbar.vue"

export default {
  name: 'App',
  components: {
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

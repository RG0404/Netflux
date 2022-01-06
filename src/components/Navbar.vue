<template>
  
    <nav>

        <div class="main-container">

            <div class="left-container">
                <img :src="image" alt="logo" class="logo-netflux">
                <div class="menu-items">
                    <a href="#">Accueil</a>
                    <a href="#">Séries</a>
                    <a href="#">Films</a>
                    <a href="#">Nouveautés les plus regardées</a>
                    <a href="#">Ma liste</a>
                </div>
            </div>

            <div class="right-container">

            </div>

        </div>

    </nav>
  
</template>

<script>

export default {
  name: 'Navbar',
  components: {
    
  },
  props: [
      'image'
  ]
}

</script>

<style>

    nav {
        height: 70px;
        widows: 100%;
        background-color: green;
    }

    .logo-netflux {
        widows: 100px;
        height: 38px;
    }

    .menu-items {
        display: flex;
        gap: 12px;
    }

    .menu-items a {
        color: #fff;
        font-size: 12px;
    }

    .left-container {
        display: flex;
        align-items: center;
    }

</style>

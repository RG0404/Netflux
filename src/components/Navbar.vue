<template>
  
    <nav class="opacity-0">

        <div class="main-container">

            <div class="left-container">
                <img :src="logo" alt="logo" class="logo-netflux">
                <div class="menu-items">
                    <a href="#">Accueil</a>
                    <a href="#">Séries</a>
                    <a href="#">Films</a>
                    <a href="#">Nouveautés les plus regardées</a>
                    <a href="#">Ma liste</a>
                </div>
            </div>

            <div class="right-container">
                <i class="fas fa-search"></i>
                <a href="#">DIRECT</a>
                <i class="fas fa-bell"></i>
                <img :src="profile" alt="profile" class="profile-photo">
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
      'logo',
      'profile',
  ]
}

let scrollpos = window.scrollY

window.addEventListener('scroll', function() {
    scrollpos = window.scrollY;
    let header = document.querySelector("nav");
    if (scrollpos > 0 && header.classList.contains('opacity-0')) {
        header.classList.add('opacity-1');
        header.classList.remove('opacity-0');
    } else if (scrollpos == 0) {
        header.classList.add('opacity-0');
        header.classList.remove('opacity-1');
    }
})

</script>

<style scoped>

    nav {
        height: 70px;
        widows: 100%;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        z-index: 10;
        transition: all;
        transition-duration: 500ms;
    }

    .opacity-0 {
        background-color: rgba(20, 20, 20, 0)
    }

    .opacity-1 {
        background-color: rgba(20, 20, 20, 1)
    }

    .main-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 70px;
    }

    .logo-netflux {
        widows: 100px;
        height: 38px;
    }

    .menu-items {
        display: flex;
        gap: 12px;
        margin-left: 30px;
    }

    .menu-items a {
        color: #fff;
        font-size: 12px;
    }

    .left-container {
        display: flex;
        align-items: center;
        margin-left: 30px;
    }

    .right-container {
        display: flex;
        align-items: center;
        margin-right: 60px;
        gap: 20px;
    }

    .right-container i {
        color: #fff;
        height: 18px;
        widows: 26px;
    }

    .right-container a {
        font-size: 12px;
        color: #fff;
    }

    .profile-photo {
        width: 32px;
        height: 32px;
        border-radius: 18%;
    }

</style>

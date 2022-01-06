<template>
  
    <div class="hero-container">

        <div class="hero-content">

            <img src="../assets/hero-title.webp" alt="">
            <div class="hero-p">Dans ce drame inspiré de faits réels, un adolescent de Détroit devient indic pour le FBI puis dealer de drogue, au plus fort de "l'épidémie du crack" des années 1980.</div>
            <div class="hero-buttons">
                <a href="#">
                    <div class="button-play">
                        <i class="fas fa-play"></i>
                        <div class="button-play-p">Lecture</div>
                    </div>
                </a>
                <a href="#">
                    <div class="button-info">
                        <i class="fas fa-info-circle"></i>
                        <div class="button-info-p">Plus d'infos</div>
                    </div>
                </a>
            </div>
            <div class="hero-warning">
                <div class="hero-refresh">
                    <i class="fas fa-redo"></i>
                </div>
                <div class="hero-age">
                    <div class="hero-warning-hr"></div>
                    <div class="hero-warning-box">
                        <p>16+</p>
                    </div>
                </div>
            </div>

        </div>

    </div>
  
</template>

<script>

export default {
  name: 'HeroBanner',
  components: {
    
  },
  props: [
      
  ]
}

</script>

<style scoped>

    .hero-container {
        position: relative;
        width: 100%;
        height: 100vh;
        /* margin-top: 70px; */
        background-image: linear-gradient(to bottom, rgba(20, 20, 20, 0),  rgba(20, 20, 20, 1)), linear-gradient(to top, rgba(20, 20, 20, 0),  rgba(20, 20, 20, 0.5)), url(../assets/hero-banner.jpg);
        background-size: cover;
        display: flex;
        align-items: center;
    }

    .hero-content {
        width: 420px;
        margin-left: 30px;
        color: #fff;
    }

    .hero-content img {
        width: 420px;
        margin-top: -100px;
    }

    .hero-p {
        margin-top: 20px;
        font-size: 17px;
    }

    .hero-buttons {
        display: flex;
        margin-top: 20px;
        gap: 20px;
    }

    .button-play {
        width: 136px;
        height: 40px;
        background-color: #fff;
        color: #000;
        border-radius: 4px;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 16px;
        font-size: 16px;
        font-weight: bold;
    }

    .button-play i {
        font-size: 20px;
    }

    .button-info {
        width: 164px;
        height: 40px;
        background-color: rgba(109,109,110,0.9);
        color: white;
        border-radius: 4px;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 16px;
        font-size: 16px;
        font-weight: bold;
    }

    .button-info i {
        font-size: 20px;
    }

    .hero-warning {
        position: absolute;
        right: 0;
        top: 60vh;
        display: flex;
        align-items: center;
    }

    .hero-refresh {
        width: 38px;
        height: 38px;
        border-radius: 50%;
        border: 0.5px solid #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 13px;
        margin-right: 20px;
    }

    .hero-age {
        width: 78px;
        height: 28px;
        display: flex;
    }

    .hero-warning-hr {
        height: 28px;
        width: 3px;
        background-color: #fff;
    }

    .hero-warning-box {
        background-color: rgba(20, 20, 20, 0.5);
        width: 78px;
        display: flex;
        align-items: center;
        font-size: 12px;
    }

    .hero-warning-box p {
        margin-left: 8px;
    }

</style>

<template>

  <div class="social-links">
    <img src="../assets/facebook.png" alt="">
    <img src="../assets/linkedin.png" alt="">
    <img src="../assets/twitter.png" alt="">
    <img src="../assets/github.png" alt="">
  </div>

  <div class="footer">
    <div class="first-grid">
      <li>Audiodescription</li>
      <li>Relation Investisseurs</li>
      <li>Informations légales</li>
    </div>

    <div class="second-grid">
      <li>Centre d'aide</li>
      <li>Recrutement</li>
      <li>Préférences des cookies</li>
    </div>

    <div class="third-grid">
      <li>Cartes cadeaux</li>
      <li>Conditions d'utilisation</li>
      <li>Mentions légales</li>
    </div>

    <div class="fourth-grid">
      <li>Presse</li>
      <li>Confidentialité</li>
      <li>Nous contacter</li>
    </div>
  </div>

</template>

<script>
  export default {
    name: 'Footer'
  }
</script>

<style scoped>

.social-links {
  display: flex;
  margin-bottom: 30px;
  margin-left: 8%;
  gap: 10px;
}

.social-links img {
  width: 45px;
  height: 45px;
}

.footer {
  display: grid;
  grid-template-columns: auto auto auto auto;
  background-color: rgb(20, 20, 20);
  text-align: center;
  margin-bottom: 10%;
}

li {
  list-style: none;
  color: grey;
  margin-top: 15px;
}


</style>
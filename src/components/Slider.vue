<template>
  <div>
    <h1>Top 250 des meilleurs films</h1>
    <section class="carousel">
      <img
          v-for="item in movies.slice(0, 100)"
          :key="item.id"
          :src="item.image"
      />
    </section>

    <h1>Top Séries</h1>
    <section class="carousel">
      <img
          v-for="item in series.slice(0, 100)"
          :key="item.id"
          :src="item.image"
      />
    </section>

    <h1>Les plus populaires</h1>
    <section class="carousel">
      <img
          v-for="item in popular.slice(0, 100)"
          :key="item.id"
          :src="item.image"
      />
    </section>

    <h1>Coming Soon..</h1>
    <section class="carousel">
      <img
          v-for="item in soon.slice(0, 100)"
          :key="item.id"
          :src="item.image"
      />
    </section>
  </div>
</template>

<script>
  export default {
    name: 'Slider',
    props: [
        'movies',
        'series',
        'soon',
        'popular',
    ]
  }
</script>

<style scoped>

.carousel {
  margin-top: 5%;
  margin: 2rem 2rem 6rem;
  display: flex;
  overflow: scroll;
}

.carousel::-webkit-scrollbar {
  display: none;
}

img {
  width: 400px;
  height: 400px;
  margin: 20px;
  transition: ease-in-out;
  transition-duration: 200ms;
}

img:hover {
  transform: scale(1.1);
}

h1 {
  font-size: 2rem;
  line-height: 1;
  color: #fff;
  margin-left: 20px;
}

</style>
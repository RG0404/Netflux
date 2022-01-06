<template>
  <div>
    <section class="carousel">
      <h1>Top 250 des meilleurs films</h1>
      <ul class="carousel-items">
        <li class="carousel-item" v-for="item in movies" :key="item.id">
          <div class="card">
            <h2 class="card-title" >{{ item.title }}</h2>
            <img :src="item.image" >
          </div>
        </li>
      </ul>

      <ul class="carousel-items">
        <li class="carousel-item" v-for="item in series" :key="item.id">
          <div class="card">
            <h2 class="card-title" >{{ item.title }}</h2>
            <img :src="item.image" >
          </div>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
  export default {
    name: 'Slider',
    props: [
        'movies',
        'series'
    ]
  }
</script>

<style scoped>

.carousel {
  margin-top: 5%;
  margin: 2rem 2rem 1rem;
}

h1 {
  font-size: 2rem;
  line-height: 1;
  color: #fff;
}

h2 {
  font-size: 1.25rem;
  margin-top: 0;
  color: #fff;
}

ul {
  margin: 0 0 1.5rem;
  padding: 0;
}

li {
  display: inline-block;
}

svg {
  fill: currentColor;
  width: 1.5rem;
  height: 1.5rem;
}

img {
  height: auto;
  margin-bottom: .5rem;
  max-width: calc(100% + 2rem);
  position: relative;
  left: -1rem;
  right: -1rem;
}

p {
  margin: 0 0 .5rem;
}

main {
  padding: 1rem 2rem;
  margin: auto;
}

header {
  padding: 1rem 2rem;
  text-align: center;
}

.card {
  border: 1px solid #bac6d3;
  border-radius: 8px;
  padding: 1rem;
}

.card img {
  width: 400px;
  height: 300px;
}

/********************************
* Carousel styles
*********************************/
.carousel-items {
  display: flex;
  overflow-x: scroll;
  padding: 1rem 0;
  scroll-snap-type: x mandatory;
  margin-top: 5%;
}

.carousel-item {
  flex: 1 0 250px;
  margin-left: 1rem;
  scroll-snap-align: start;
}

::-webkit-scrollbar-track {
  background-color: #F5F5F5;
}

::-webkit-scrollbar {
  height: 6px;
  background-color: #F5F5F5;
}

::-webkit-scrollbar-thumb {
  background-color: #3d4852;
  border-radius: 3px;
}

</style>
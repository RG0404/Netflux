<template>
  <div>
    <section class="carousel">
      <ul class="carousel-items">
        <li class="carousel-item">
          <div class="card">
            <h2 class="card-title" v-for="movie in movies" :key="movie.id">{{ movie.rank}}</h2>
            <img src="https://placeimg.com/572/322/animals" alt=""/>
          </div>
        </li>
        <li class="carousel-item">
          <div class="card">
            <h2 class="card-title"></h2>
            <img src="https://placeimg.com/572/322/animals" alt=""/>
          </div>
        </li>
        <li class="carousel-item">
          <div class="card">
            <h2 class="card-title"></h2>
            <img src="https://placeimg.com/572/322/animals" alt=""/>
          </div>
        </li>
        <li class="carousel-item">
          <div class="card">
            <h2 class="card-title"></h2>
            <img src="https://placeimg.com/572/322/animals" alt=""/>
          </div>
        </li>
        <li class="carousel-item">
          <div class="card">
            <h2 class="card-title"></h2>
            <img src="https://placeimg.com/572/322/animals" alt=""/>
          </div>
        </li>
        <li class="carousel-item">
          <div class="card">
            <h2 class="card-title"></h2>
            <img src="https://placeimg.com/572/322/animals" alt=""/>
          </div>
        </li>
        <li class="carousel-item">
          <div class="card">
            <h2 class="card-title"></h2>
            <img src="https://placeimg.com/572/322/animals" alt=""/>
          </div>
        </li>
        <li class="carousel-item">
          <div class="card">
            <h2 class="card-title"></h2>
            <img src="https://placeimg.com/572/322/animals" alt=""/>
          </div>
        </li>
        <li class="carousel-item">
          <div class="card">
            <h2 class="card-title"></h2>
            <img src="https://placeimg.com/572/322/animals" alt="" />
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
    ]
  }
</script>

<style scoped>

h1 {
  font-size: 2rem;
  margin: 2rem auto 1rem;
  line-height: 1;
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

/********************************
* Carousel styles
*********************************/
.carousel-items {
  display: flex;
  overflow-x: scroll;
  padding: 1rem 0;
  scroll-snap-type: x mandatory;
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
<template>
  <div class="flex-div">
    <div v-for="(movie, index) in movies" :key="index" class="flex-container clickable-div" @click="handleClick(movie)">
      <div class="card">
        <img :src="movie.poster_url" :alt="movie.title">
        <h3>{{movie.title}}</h3>
        <p>{{ movie.release_year }}</p>
        <p>{{ movie.genre }}</p>
        <p>{{ movie.rating }}</p>
      </div>
    </div>
  </div>
</template>
  
<script setup>
import { ref } from 'vue';
import { MOVIES } from '../moviedata';
const movies = ref(MOVIES);

const handleClick = (movie) => {
  console.log(movie.poster_url);
  if (movie && movie.poster_url) {
    window.location.href = movie.poster_url;
  } else {
    console.error('Invalid movie data');
  }
}
</script>
  
<style scoped>
.flex-div {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 20px;
}

.flex-container {
  width: 300px;
  margin: 10px;
}

.card {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  padding: 15px;
  text-align: center;
  min-height: 530px;
  max-height: 530px;
}

img {
  max-width: 100%;
  border-radius: 6px;
  height: 300px;
}

h3 {
  font-size: 1.5em;
}

p {
  margin: 5px 0;
}

.clickable-div {
  cursor: pointer;
  padding: 10px;
  background-color: lightblue;
}
</style>
  
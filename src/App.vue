<script setup>
import HeaderPage from './components/Header.vue'
import MoviePage from './components/MoviePage.vue';
import FooterPage from './components/Footer.vue';
</script>

<template>
 <div>
   <HeaderPage class="headerPage"/>

  <main>
    <MoviePage :movies="MOVIES" class="moviePage"/>
  </main>
  <FooterPage />
 </div>
</template>

<style scoped>
.moviePage{
  padding: 20px 0;
  margin-bottom: 30px;
}
.headerPage{
  padding-bottom: 20px;
}
</style>

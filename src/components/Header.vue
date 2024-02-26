<template>
  <div class="marvel-header">
    <nav class="navbar">
      <div class="logo logotext">{{ title }}</div>
      <ul class="nav-links">
        <li>Home</li>
        <li>Movies</li>
      </ul>
    </nav>
    <p>{{ description }}</p>
  </div>
</template>
  
<script setup>
const title = "Marvel Movies";
const description = "Explore the Marvel Universe!";
</script>
  
<style scoped>
.marvel-header {
  background-color: #0e0d0d;
  padding: 20px;
  text-align: center;
}

.logotext {
  color: #ed1d24;
  font-size: 2em;
}

p {
  color: rgb(117, 110, 110);
  font-size: 1.2em;
  text-align: left;
}

.navbar {
  background-color: #333;
  color: #fff;
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.5em;
}

.nav-links {
  list-style: none;
  display: flex;
}

.nav-links li {
  margin-right: 15px;
}

.nav-links a {
  text-decoration: none;
  color: #fff;
}
</style>
  
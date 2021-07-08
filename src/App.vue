<template>
  <div id="app">
    <app-navbar/>
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->
    <!-- </div> -->
    <router-view/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
export default {
  components: {
    appNavbar: Navbar
  }
}
</script>

<style>
@font-face {
  font-family: 'Gotham';
  src: local('Gotham'), url('./assets/Gotham-Font/GothamMedium.ttf'), format('truetype');
}
body{
  padding: 0 !important;
  margin: 0;
}
#app {
  font-family: 'Gotham';
  padding: 0;
  margin: 0;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<template>
  <div id="app">
    <navbar></navbar> <!-- Add the navbar component or custom navbar -->
    <div class="container">
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Tab's Homepage"/>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue' // Import the navbar component or update with the correct path

export default {
  name: 'App',
  components: {
    HelloWorld,
    Navbar // Add the navbar component to the components section
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}
</style>
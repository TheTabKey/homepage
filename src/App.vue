<template>
  <div id="app">
    <div class="vanta-background" ref="vantaRef">
      <navbar></navbar>
      <div class="container">
        <img alt="Vue logo" src="./assets/logo.png">
        <HelloWorld msg="Tab's Homepage"/>
      </div>
    </div>
    </div>
</template>

<script>
/* eslint-disable vue/no-deprecated-destroyed-lifecycle */

import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue' // Import the navbar component or update with the correct path
import BIRDS from 'vanta/dist/vanta.waves.min'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Navbar
  },
  mounted() {
    this.vantaEffect = BIRDS({
      el: this.$refs.vantaRef
    })
  },
  beforeDestroy() {
    if (this.vantaEffect) {
      this.vantaEffect.destroy()
    }
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
  margin-top: 0 !important;
  padding-top: 0 !important;
}

.vanta-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}
</style>
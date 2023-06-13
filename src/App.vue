<template>
  <div id="app">
    <div class="vanta-background" ref="vantaRef">
      <navbar></navbar>
      <div class="container">
        <div class="centered-content">
          <img alt="Vue logo" src="./assets/logo.png" class="vw-img">
          <HelloWorld msg="Tab's Homepage"/>
        </div>
      </div>
    </div>
    </div>
</template>

<script>
/* eslint-disable vue/no-deprecated-destroyed-lifecycle */

import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue'
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
  margin-top: 0;
  padding-top: 0;
}
.vanta-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

.centered-content {
  text-align: center;
}
.vw-img {
  width: 30vw;
}
</style>
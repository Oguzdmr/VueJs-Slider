<template>
  <div id="app">
    <NavBar msg="Welcome to Your NavBar App" />
    <Carousel msg="Welcome to Your Carousel App"/>
  </div>
</template>

<script>
import Carousel from './components/Carousel.vue'
import NavBar from './components/Navbar'


export default {
  name: 'App',
  components: {
    Carousel:Carousel,
    NavBar:NavBar
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
  margin-top: 60px;
}
</style>

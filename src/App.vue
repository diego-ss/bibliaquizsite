<template>
  <div id="app">
    <Navbar></Navbar>
    <Home></Home>
    <Contact></Contact>
    <BibleVerse></BibleVerse>
    <br>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import Contact from './components/Contact.vue'
import BibleVerse from './components/BibleVerse.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Home,
    Contact,
    BibleVerse
  },
  
  created(){
    document.title = "BibliaQuizApp"
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
  padding: 0px;
  margin: 0px;
  box-sizing: border-box;
}
</style>

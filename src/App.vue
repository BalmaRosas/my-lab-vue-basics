<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <NavBar/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <MyFooter/>
   
  </div>
  
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import NavBar from './components/NavBar.vue'
import MyFooter from './components/MyFooter.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
    NavBar,
    MyFooter
  },

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

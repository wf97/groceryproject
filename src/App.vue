<template>
  <div id="app">
    <app-header v-bind:title="msg"></app-header>
    <router-view></router-view>
    <app-footer></app-footer>
  </div>
</template>

<script>
//Registering components Locally
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    //Registering with a name
    'app-header':Header,
    'app-footer':Footer,
    //Registering without a name
  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
</style>

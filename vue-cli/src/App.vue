<template>
  <!-- The template root requires exactly one element. -->
  <div id="app">
    {{ str }}
    <app-header></app-header>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import AppHeader from "./components/AppHeader.vue";

// var AppHeader = {
//   template: '<header><h1>Header</h1></header>'
// }

// new Vue({
//   data: {
//     str: 'hi'
//   }
// })

export default {
  name: 'App',
  components: {
    HelloWorld,
    // 'hello-world': HelloWorld,
    'app-header': AppHeader,
  },
  data: function() {
    return {
      str: 'hi'
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
  margin-top: 60px;
}
</style>

<template>
  <!-- The template root requires exactly one element. -->
  <div id="app">
    {{ str }}
    <!-- 프롭스 속성 이름 : 하위 컴포넌트에서 정의한 속성 이름 -->
    <!-- 현재 상위 컴포넌트 : App.vue -->
    <!-- <app-header v-bind:프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header> -->
    <app-header
        v-bind:propsdata="str"
        v-on:renew="renewStr"></app-header>
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
      str: 'Header'
    }
  },
  methods: {
    renewStr: function () {
      this.str = 'hi';
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

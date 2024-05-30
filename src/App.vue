<template>
  <TheHeader v-if="showHeader"/>

  <div v-show="showName">
    Nome: {{ firstnName }} <br>
    Nome: {{ lastName }}
  </div>

  <div v-if="acessLevel === 'admin'"> Admin </div>
  <div v-else-if="acessLevel === 'marketing'"> Marketing </div>
  <div v-else >Usuario norma</div>

  <img  
    alt="Vue logo" src="./assets/logo.png">
  
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue'

export default {
  name: 'App',
  components: {
    HelloWorld, TheHeader
  },
  data() {
    return {
      showHeader: false,
      firstnName: 'Jon',
      lastName: 'Snow',
      showName: false,
      acessLevel: 'marketing'
    
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

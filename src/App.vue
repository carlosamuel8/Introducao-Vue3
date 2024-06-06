<template>
  <TheHeader v-if="showHeader"/>

  <!-- <div v-show="showName">
    Nome: {{ firstnName }} <br>
    Nome: {{ lastName }}
  </div>

  <div v-if="acessLevel === 'admin'"> Admin </div>
  <div v-else-if="acessLevel === 'marketing'"> Marketing </div>
  <div v-else >Usuario norma</div> -->
<!-- 
  <img  
    alt="Vue logo" src="./assets/logo.png">
  
  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  
  <h1 :class="classvar" ></h1>


  <div 
    v-for="(obj, index) in todos" 
    :key="obj.id" 
    class="todo-item"
    >
     {{index}} - {{ obj.title }}
  </div>

  <div>
    <label>contrato</label> <br>
    <input  
      v-model="contract"
      type="checkbox"
    >
    Aceita nossos termos <br>
    {{ contract }}
  </div>

  <div>
    <label>Your favorite colors</label> <br>
    <input  
      v-model="colors"
      type="checkbox"
      value="Amarelo"
    >
    Amarelo <br>

    <input  
      v-model="colors"
      type="checkbox"
      value="Azul"
    >
    Azul <br>
    {{ colors }}
  </div>
  <div>
    <button @click="onclick">
      enviar
    </button>
  </div>

  <div>
    <h1> {{ fullName }} </h1>
  </div>

</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import TheHeader from './components/TheHeader.vue'


 
export default {
  name: 'App',
  components: {
    // HelloWorld, TheHeader
  },
  data() {
    return {
      firstName: 'João',
      lastName: 'Silva',
      colors: [],
      contract: false,
      classvar: 'title',
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
        ]    
    }
  },

  methods: {
    onclick(){
      console.log('clicou')
    }
  },

  computed: {
      fullName() {
        return this.firstName + ' ' + this.lastName
      
      }
  }
  

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin: 60px;
}

.todo-item {
  border: 1px solid #ccc;
  margin: 10px;
  padding: 10px;
  border-radius: 5px;
}

.title{
  color: red;
  font-size: large;
}


</style>

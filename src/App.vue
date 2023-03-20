<template>
  <img class="logo" alt="Lidera logo" src="./assets/Logo_Lidera.webp">
  <h2>Este es un saludo :)</h2>
  <Input @evento="saludar"/>
  <Saludo :message="message" />

</template>
<script>

import Input from './components/Input.vue';
import Saludo from './components/Saludo.vue';

export default {
  name: 'App',
  components: { Input, Saludo },
    data () {
      return {
        nombre: '',
        message: ''
      }
    },
    methods: {
      saludar () {
        
        this.message = 'Hola'+ this.$saludar;
        console.log(this.message)
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

img {
  max-width: 40%;
}



</style>

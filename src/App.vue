<template>
  <img class="logo" alt="Lidera logo" src="./assets/Logo_Lidera.webp">
  <h2>Este es un saludo</h2>
  <div class="wrapper">
    <Input @clicked="onClickChild"/>
    <Saludo :message="message" />
  </div>

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
      onClickChild (name) {
        
        this.message = 'Hola '+ name + " :)";
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
  max-width: 30%;
}



</style>

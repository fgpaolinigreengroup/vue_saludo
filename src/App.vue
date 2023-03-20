<template>
    <div class="wrapper">
    <img class="logo" alt="Lidera logo" src="./assets/Logo_Lidera.webp">
    <h2>Este es un saludo</h2>
    <Input class="childComponent" @clicked="onClickChild"/>
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


}

img {
  max-width: 50%;
  margin-top: 10px;
}

.childComponent {
  padding: 0 300px;
}

.wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 400px;
    height: fit-content;
    margin-top: 100px;
    background-color: #2c3e50;
    border-radius: 20px;
    box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
}

h2 {
    background-color: #0f2027;
    color: #fff;    
    padding: 5px 20px;
    border-radius: 10px;
    font-family: 'Roboto', sans-serif;
    font-size: 2em;
    color: #EC5C5F;
}

body {
  display: flex;
  align-items: top;
  justify-content: center;
  height:100vh;
  background: #0f2027; /* fallback for old browsers */
  background: linear-gradient(to right,#2c5364, #203a43, #0f2027);
  color: #fff;
  box-sizing: border-box;
  margin: 0;
  padding: 0;

}
</style>

<template>
    <div>
        <label>¿Cómo te llamas?</label>
        <input type="text" required v-model="nombre">
    </div>
    <button @click="onClickedButton($event)">Saludo</button>
<!--     <p>{{ nombre }}</p>
-->

</template>

<script>
    export default {
        emits: ['clicked'],
        data() {
            return {
                nombre: null
            }
        },
        methods: {
            onClickedButton(event){
                console.log("Este es el nombre: " + this.nombre);
                this.$emit('clicked', this.nombre)
            }
        }
        
    }

</script>
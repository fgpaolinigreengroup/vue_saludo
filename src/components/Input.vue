<template>
    <div>
        <label>¿Cómo te llamas?</label>
        <input type="text" required v-model="nombre">
    </div>
    <button @click="emitirEvento">Saludo</button>
    <p>{{ nombre }}</p>


</template>

<script>
    export default {
        emits: ['nombre'],
        data() {
            return {
                nombre: ''
            }
        },
        methods: {
            emitirEvento(){
                this.$emit(this.nombre)
            }
        }
        
    }

</script>
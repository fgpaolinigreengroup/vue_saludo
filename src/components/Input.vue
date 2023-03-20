<template>
    <div>
        <h2>¿Cómo te llamas?</h2>
        <input type="text" required v-model="nombre">
        <button @click="onClickedButton($event)">Saludo</button>
    </div>
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

<style scoped>

h2 {
    background-color: unset;
    font-family: 'Roboto', sans-serif;
    font-size: 1.2rem;
    color: #eee;
    
}

input {
    font-family: 'Roboto', sans-serif;
    color: #333;
    font-size: 1.2rem;
    margin: 10px auto;
    border-radius: 0.2rem;
    background-color: rgb(255, 255, 255);
    border: none;
    height: 30px;
    display: block;
    border-bottom: 0.3rem solid transparent;
    transition: all 0.3s;
}

button {
    align-items: center;
    appearance: none;
    background-color: #fff;
    border-radius: 24px;
    border-style: none;
    box-shadow: rgba(0, 0, 0, .2) 0 3px 5px -1px,rgba(0, 0, 0, .14) 0 6px 10px 0,rgba(0, 0, 0, .12) 0 1px 18px 0;
    box-sizing: border-box;
    color: #3c4043;
    cursor: pointer;
    display: inline-flex;
    fill: currentcolor;
    font-family: "Google Sans",Roboto,Arial,sans-serif;
    font-size: 14px;
    font-weight: 500;
    height: 40px;
    justify-content: center;
    letter-spacing: .25px;
    line-height: normal;
    max-width: 100%;
    overflow: visible;
    padding: 2px 24px;
    position: relative;
    text-align: center;
    text-transform: none;
    transition: box-shadow 280ms cubic-bezier(.4, 0, .2, 1),opacity 15ms linear 30ms,transform 270ms cubic-bezier(0, 0, .2, 1) 0ms;
    user-select: none;
    -webkit-user-select: none;
    touch-action: manipulation;
    width: 100%;
    will-change: transform,opacity;
    z-index: 0;
}

    button:hover {
    background: #F6F9FE;
    color: #174ea6;
    }


    button:active {
    box-shadow: 0 4px 4px 0 rgb(60 64 67 / 30%), 0 8px 12px 6px rgb(60 64 67 / 15%);
    outline: none;
    }

    button:focus {
    outline: none;
    border: 2px solid #4285f4;
    }

    button:not(:disabled) {
    box-shadow: rgba(60, 64, 67, .3) 0 1px 3px 0, rgba(60, 64, 67, .15) 0 4px 8px 3px;
    }

    button:not(:disabled):hover {
    box-shadow: rgba(60, 64, 67, .3) 0 2px 3px 0, rgba(60, 64, 67, .15) 0 6px 10px 4px;
    }

    button:not(:disabled):focus {
    box-shadow: rgba(60, 64, 67, .3) 0 1px 3px 0, rgba(60, 64, 67, .15) 0 4px 8px 3px;
    }

    button:not(:disabled):active {
    box-shadow: rgba(60, 64, 67, .3) 0 4px 4px 0, rgba(60, 64, 67, .15) 0 8px 12px 6px;
    }

    button:disabled {
    box-shadow: rgba(60, 64, 67, .3) 0 1px 3px 0, rgba(60, 64, 67, .15) 0 4px 8px 3px;
    }

</style>
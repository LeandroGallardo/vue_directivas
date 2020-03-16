<template>
    <button @click="nuevoMensaje"> Nuevo mensaje </button>
</template>

<script>
import eventBus from '../eventBus'
export default {
    name: 'BrotherComponent',
    methods:{
        nuevoMensaje(){
            eventBus.$emit('nuevomensaje', 'hola soy el bus evento')
        }
    }
}
</script>

<style>

</style>
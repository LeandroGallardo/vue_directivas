<template>
<div>
    <h1>{{newMessage}}</h1>
    <slot name="mainSlot"/>
       <h3>papa johns o piiza huts</h3>

    <button @click="emitNewMessage"> cambiar mensaje</button>
</div>
</template>


<script>
import eventBus from '../eventBus'
export default {
    name:'ChieldComponent',
    props: {
        newMessage: {
            type: String,
            validator: value =>{
                return value.includes('pizza')
            }

        }
    },
    methods:{
        emitNewMessage(){
            this.$emit('changeMessage', 'queremos mas pizza')
        }
    },
    created(){
        eventBus.$on('nuevomensaje',(event)=>{
            this.newMessage = event
        })
    }
}
</script>

<style>

</style>
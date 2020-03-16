<template>
  <div id="app">
    <ChieldComponent v-bind:newMessage="message" @changeMessage="cambiandomensaje">
      <!--template v-slot:mainSlot>
         <h2>que sabor de pizza te gusto más</h2>
      </template-->
      
    </ChieldComponent>
    <BrotherComponent/>
  
  </div>
</template>

<script>
import ChieldComponent from './components/ChildComponent'
import BrotherComponent from './components/BrotherComponent'
export default {
  name: 'App',
  components: {
    ChieldComponent,
    BrotherComponent
  },
  data(){
    return{
      message : 'que rico estuvo la pizza'
    }
  },
  methods:{
    cambiandomensaje(evento){
      console.log(evento)
      this.message= evento
    }
  }
}
</script>

<style>

</style>

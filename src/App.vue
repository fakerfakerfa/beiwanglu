<template>
  <div>
     <Tou  :todos="todos"></Tou>
     <Shen :parent="todos"></Shen>
        <Wei :shuliang="todo"></Wei>

  </div>
</template>

<script>
import Tou from './tou.vue'
import Shen from './shenti.vue'
import Wei from './weibu.vue'

  export default {
    props: {

    },
    components: {
      Tou,
      Shen,
      Wei,
    },
    data(){
      return {
        todos:[
                 {cc:'吃饭',completed:false},
                 {cc:'睡觉',completed:false},
                 {cc:'打游戏',completed:true},
               ],

         todo:''
         
          }
      
       },
    methods: {
       
    },
    watch:{
       todos:{
        handler(){
           this.todo=this.todos.length
        },
        immediate:true
       }
    },
   
  }
</script>

<style>

</style>

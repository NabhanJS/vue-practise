<template>
  <div id="app">
    

     <ul>
       <li v-for="fruit in fruits" v-bind:key="fruit">  {{fruit}} </li>
  
    </ul>
   
  </div>
</template>

<script>


export default {
  name: 'App',
  
  data(){
       return{
           fruits: ['Orange', 'Banana', 'Mango']
       }
   },

}
</script>

<style>

</style>

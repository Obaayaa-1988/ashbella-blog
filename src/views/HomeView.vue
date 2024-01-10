<template>
  <div class="home">
  <p ref="p">My name is: {{ name }} and I am {{ age }} years old</p>
  <button @click="buttonClicked">Click me</button>
  </div>
</template>

<script>
import { ref } from 'vue';
// @ is an alias to /src

export default {
  name: 'HomeView',
  //composition api// this function runs before any lifecycle hooks
 setup(){
  console.log('setup')
  const p = ref(null)
  let name = 'Eno Mary';
  let age = 2;

  //writing arrow functions
  const buttonClicked = () => {
    console.log('you clicked me')
  }

  return {name: name, age: age, buttonClicked, p}// not reactive values

 },

//  data(){
//   return{
//     career: 'doctor'// reactive values
//   }
//  }
//  created(){
//   console.log('created')

//  },
//  mounted(){
//   console.log('mounted')

//  },
}
</script>

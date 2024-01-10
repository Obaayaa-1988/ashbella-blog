<template>
  <div class="home">
  <p>My name is: {{ name }} and I am {{ age }} years old</p>
  <button @click="buttonClicked">Click me</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  //composition api// this function runs before any lifecycle hooks
 setup(){
  console.log('setup')
  let name = 'Eno Mary';
  let age = 2;

  //writing arrow functions
  const buttonClicked = () => {
    console.log('you clicked me')
  }

  return {name: name, age: age, buttonClicked}// not reactive values

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

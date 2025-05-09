<template>
    <div :class="dog.age > 3 ? 'green' : 'red'">
      <h2>{{ dog.breed_name }}</h2>
      <h3>{{ dog.breed_group }}</h3>
      <h3>{{ dog.color }}</h3>  
      <h3>{{ dog.temperament }}</h3>
      <h3>{{ dog.life_expectancy }}</h3>
      <h3>{{ dog.species }}</h3>
      <h3>{{ dog.age }}</h3>
    </div>
    
  </template>
  
  <script>
  export default {
    name: 'SingleDog',
    props: {
      dog: Object  // Ensure that 'dog' is passed as an object
    }
  }
  </script>
  
  <style scoped>

  
  .green {
    background-color: rgb(109, 212, 99); 
  }
  
  .red {
    background-color: rgb(243, 185, 77); 
  }
  
  h4 {
    margin: 2px;
  }
  
  div {
    background-color: #ffb89e; 
    color: black;
   
    text-align: center;
    width: 80%;
    margin: auto;
    border-radius: 8px;
  }
  </style>
  
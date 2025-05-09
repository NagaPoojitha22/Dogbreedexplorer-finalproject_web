<template>
  <div v-for="item in dog" :key="item.id">
    <SingleDog :dog="item" />
  </div>
</template>


<script>
import SingleDog from './SingleDog.vue'
//import dogData from '../db.json'

export default {
  name: 'DogBox',
  props: {
    dog: Array
  },
  components: { SingleDog },
  
}
</script>


<style scoped>

div{
    text-align: center;
}

</style>
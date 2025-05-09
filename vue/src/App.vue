<template>
  <MyHeader Name="Dog Breed Explorer" authorName="Naga Poojitha Konda" />
  <DogBox :dog="dog" />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import DogBox from './components/DogBox.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    DogBox
  },
  data() {
    return {
      dog: [] // data to hold dog data from API
    }
  },
  created()
    {
      this.fetchdog()
    },
  
  methods: {
    async fetchdog() {
      const res = await fetch("https://poojithakondanodejs-ovcb.onrender.com/api");
      const data = await res.json();
      console.log(data); // Check if you get the correct dog data
      this.dog = data;
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div {
  margin-bottom: 0.5em;
  text-align: center;
}
</style>

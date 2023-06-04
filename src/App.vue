<template>
  <div id="app">
    <h1>{{ message }}</h1>
    <div>
    <input type="file" accept="image/*" multiple>
    </div>
    <div v-if="url">
  <img :src="url">
</div>
    
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
  return {
    message:"Try Preview!",
    url:""
  }
},
  mounted(){
  console.log(this.$refs.preview)
},
methods:{
  uploadFile(){
    console.log(this.$refs.preview.files[0])
  }
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{msg}}</h1>
  </div>
</template>

<script>
import {observable} from './Rx'
export default {
  name: 'App',
  data(){
    return{
      msg:''
    }
  },
  mounted(){
    observable.subscribe((res)=>{
      this.msg = res
    })
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

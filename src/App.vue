<template>
  <div id="app">
    <AppBar/>
  </div>
</template>

<script>
import AppBar from './components/AppBar'
export default {
  name: 'app',
  components:{
    AppBar
  }
}
</script>

<style>
#app{
  font-family: Arial, Helvetica, sans-serif;
}
</style>

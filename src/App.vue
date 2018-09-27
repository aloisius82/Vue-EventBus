<template>
  <div id="app">
    <ContMessage />
    <ContControl  />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ContMessage from './components/ContMessage';
import ContControl from './components/ContControl';

export default {
  name: 'app',
  components: {
    ContMessage,
    ContControl
  },
  methods:{
    handlerEvent(evt){
      console.log('App event', evt)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <MButton content="1" @on-click="handleClick"></MButton>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MButton from './components/MButtom'
export default {
  name: 'app',
  components: {
    HelloWorld,
    MButton
  },
  methods:{
    handleClick(event){
      // eslint-disable-next-line no-console
      console.log(event["name"] + event["age"] + " 我是父组件，我拿到事件了")
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

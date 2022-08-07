<template>
  <div id="app">
    <component-header/>
    <img src="./assets/logo.png">
    <!-- // <HelloWorld/> -->
    <list-user v-bind:listUser="listUser"/>  
    <component-footer/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import ComponentHeader from './components/ComponentHeader.vue'
import ComponentFooter from './components/ComponentFooter.vue'
import ListUser from './components/ListUser.vue'

export default {
  name: 'App',
 data() {
  return {
     listUser: [
    {id:10, email: 'test1@gmail.com', active: true},
    {id:11, email: 'test2@gmail.com', active: true},
    {id:12, email: 'test3@gmail.com', active: false},
    {id:13, email: 'test4@gmail.com', active: false},
    {id:14, email: 'test5@gmail.com', active: false},
  ]
  }
 },
  components: {
    HelloWorld,
    ComponentHeader,
    ComponentFooter,
    ListUser
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

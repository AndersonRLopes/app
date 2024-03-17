<template>
  <TheHeader v-show="showHeader" />
  <div v-show="showName">
      Name: {{ name }} <br />
      Last Name: {{ lastName }}
  </div>
  <div v-if="accessLevel === 'admin'">Admin</div>
  <div v-else-if="accessLevel === 'marketing'">Marketing</div>
  <div v-else>User</div>

  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader
  },
  data(){
      return{
        showHeader: true,
        showName: true,
        name: 'Anderson',
        lastName: 'Ribeiro Lopes',
        accessLevel: 'admin'
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
</style>./components/TheHeader.Vue./components/TheHeader.vue

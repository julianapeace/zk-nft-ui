<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import { ZkIdentity } from "@zk-kit/identity"
// import { Semaphore } from "@zk-kit/protocols"
import HelloWorld from './components/HelloWorld.vue'


try {
  const identity = new ZkIdentity()
  const identityCommitment = identity.genIdentityCommitment()
  console.log(identityCommitment);
} catch (err) {
  console.log(err);
}



export default {
  name: 'App',
  components: {
    HelloWorld
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

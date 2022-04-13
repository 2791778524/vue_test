<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld/>
    <HelloworldChild/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HelloworldChild from './components/Helloworld2.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    HelloworldChild
  }
}
</script>

<style>

</style>

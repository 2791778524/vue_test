<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld/>
    <HelloworldChild ref="dom1"/>
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
  },
  mounted() {
    console.log(this.$refs.count);
    console.log(this.$children);
  }
}
</script>

<style>

</style>

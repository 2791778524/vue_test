<template>
  <div id="app">
    <!-- <HelloWorld/> -->
    <!-- <HelloworldChild ref="dom1"/> -->
    <ListSCroll />
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue'
import HelloworldChild from './components/Helloworld2.vue' */
import ListSCroll from './components/list.vue'
export default {
  name: 'App',
  components: {
    ListSCroll
  },
  mounted() {
  }
}
</script>

<style>
#app{
  height: 100%;
}
</style>

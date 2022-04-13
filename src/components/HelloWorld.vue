<template>
  <div class="hello">
    <button @click="add">传输数据</button>
  </div>
</template>

<script>
import { EventBus } from '../bus.js'
export default {
  data() {
    return {
      num: 10
    }
  },
  methods:{
    add() {
      EventBus.$emit('add',{
        num: this.num
      })
    }
  }
}
</script>

<style scoped>

</style>

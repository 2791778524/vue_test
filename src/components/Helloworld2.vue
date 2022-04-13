<template>
  <div>
      <div>兄弟组件</div>
      <h1>传过来的值为{{ count }}</h1>
  </div>
</template>

<script>
import { EventBus } from '../bus.js'
export default {
    data() {
        return {
            count: null
        }
    },
    mounted() {
        EventBus.$on('add',value => {
            this.count = value.num + 1
            console.log(this.count);
        })
        console.log(this.$parent);
    }
}
</script>

<style>

</style>
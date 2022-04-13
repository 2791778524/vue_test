<template>
  <div>
      {{ count }}
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
    }
}
</script>

<style>

</style>
<template>
  <div class="hello">
    <div>兄弟组件</div>
    <button @click="add">传输数据</button>
    <div>
      
    </div>
  </div>
</template>

<script>
import { EventBus } from '../bus.js'
export default {
  data() {
    return {
      num: 10,
      timer: null
    }
  },
  methods:{
    add() {
      this.timer = setTimeout(()=>{
        EventBus.$emit('add',{
          num: this.num
        })
      },1000)
    }
  },
  beforeMount(){},
  mounted(){},
  beforeUpdate(){},
  updated(){},
  beforeDestroy(){
    clearTimeout(timer)
    this.timer = null
  },
  destroyed(){},
}
</script>

<style scoped>

</style>

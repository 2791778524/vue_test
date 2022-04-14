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
    },
    beforeMount(){console.log('dom加载之前');},
    created() {console.log('数据加载完成后');},
    beforeCreate(){console.log('数据加载完成之前');},
    updated(){console.log('数据更新后');},
    beforeUpdate(){console.log('数据更新之前');},
    destroyed(){console.log('组件销毁后');},
    beforeDestroy(){console.log('组件销毁前');},
}
</script>

<style>

</style>
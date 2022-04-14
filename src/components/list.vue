<template>
  <recycle-scroller
    class="virtual-list"
    :buffer="1000"
    :prerender="200"
    style="height: 400px"
    :item-height="100"
    :items="tableData"
  >
    <template v-slot="{ item, index }">
      <div class="list-item" :key="item.id">
        <p class="mr-2">{{ item.id }}</p>
        <p>{{ item.name }}</p>
      </div>
    </template>
  </recycle-scroller>
</template>

<script>
export default {
  data() {
    return {
      tableData: [],
    };
  },
  created() {
    for (let i = 0; i < 100000; i++) {
      this.tableData.push({ id: i, name: Math.random() });
    }
  },
};
</script>

<style>
</style>
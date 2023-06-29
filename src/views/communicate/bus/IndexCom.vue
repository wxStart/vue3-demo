<script setup lang="ts">
import { reactive } from 'vue'
import ChildCom1 from './components/ChildCom1.vue'
import ChildCom2 from './components/ChildCom2.vue'
const info = reactive({ name: 'wahaha', age: 12 })
const changeInfo = (data): void => {
  console.log('data: ', data)
  info.name += '~!'
  info.age += 1
}
</script>

<template>
  <h3>defineEmits</h3>
  <div class="box">
    <ChildCom1 />
    <ChildCom2 />
  </div>
</template>

<style scoped>
.box {
  display: flex;
  justify-content: space-between;
}
</style>

<template>
  <ul>
    <li v-for="route in routes" :key="route.path">
      <RouterLink :to="route.path">{{ route.name }}</RouterLink>
    </li>
  </ul>
  <div>
    <RouterView />
  </div>
</template>

<script setup lang="ts">
import { RouterView, RouterLink } from 'vue-router'
interface RouteItem {
  path: string
  name: string
}
const basepath = '/communicate'
const routes: [RouteItem] = [
  {
    path: 'props',
    name: 'props'
  }
].map((el) => ({
  ...el,
  path: `${basepath}/${el.path}`
})) as [RouteItem]
</script>

<style scoped></style>

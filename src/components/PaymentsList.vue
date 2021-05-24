<template>
  <div>
    <div v-for="(item, index) in items" :key="index">
      {{item.date}}
      {{item.category}}
      {{item.price}}
    </div>
  </div>
</template>

<script>
export default {
props:{
  items:{
    type: Array,
    default:() => []
  }
}
}
</script>

<style>

</style>
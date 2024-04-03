<template>
  <input type ="text" @input="$emit('input', $event.target.value)">
  
  
  <!-- :value="searchText" @input="searchText=$event.target.value"
   равно записи  v-model = "searchText " -->
</template>

<script>
export default {
name: "myInput",
  model: {
        prop: "value",
        event: "input"
  },
};
</script>

<style>
</style>
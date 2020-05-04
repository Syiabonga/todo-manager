<template>
  <div>
      <h3>Filter Todos</h3>
      <select @change="filterTodos($event)">
        <option value="200">200</option>
        <option value="200">100</option>
        <option value="200">50</option>
        <option value="200">20</option>
        <option value="200">10</option>
        <option value="200">5</option>
      </select>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "FilterTodos",
  methods: mapActions(["filterTodos"])
};
</script>

<style>

</style>
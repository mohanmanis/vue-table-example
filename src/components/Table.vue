<template>
    <table class="table">
      <thead>
          <tr>
              <th v-for="(column, index) in columns" :key="index"> {{column}}</th>
          </tr>
      </thead>
      <tbody>
          <tr v-for="(item, index) in employees" :key="index">
              <td v-for="(column, indexColumn) in columns" :key="indexColumn">{{item[column]}}</td>
          </tr>
      </tbody>
    </table>
</template>

<script>
export default {
  name: "employee-table",
  props: {
    employees: Array,
    columns: Array
  }
};
</script>

<style scoped>
button {
  margin: 0 0.5rem 0 0;
}

input {
  margin: 0;
}

.empty-table {
  text-align: center;
}
</style>

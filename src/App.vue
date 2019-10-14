<template>
  <div id="app" class="small-container">
    <h1>Employees</h1>
    <employee-table
      :employees="employees"
      :columns="columns"
    />
  </div>
</template>

<script>
import EmployeeTable from "@/components/Table.vue";

export default {
  name: "app",
  components: {
  EmployeeTable
  },
  data() {
    return {
      employees: [
        {
          id: 1,
          name: "Richard Henricks",
          email: "richard@piedpiper.com"
        },
        {
          id: 2,
          name: "Bertram Gilfoyle",
          email: "gilfoyle@piedpiper.com"
        },
        {
          id: 3,
          name: "Dinesh Chugtai",
          email: "dinesh@piedpiper.com"
        }
      ],
      columns: ["id","name","email"]
    };
  },

};
</script>

<style>
button {
  background: #009435;
  border: 1px solid #009435;
}

button:hover,
button:active,
button:focus {
  background: #32a95d;
  border: 1px solid #32a95d;
}

.small-container {
  max-width: 680px;
}
</style>

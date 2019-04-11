<template>
  <div>
    <md-table v-model="users" :table-header-color="tableHeaderColor">
      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Name">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="City">{{ item.city }}</md-table-cell>
        <md-table-cell md-label="Salary">{{ item.salary }}</md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "simple-table",
  props: {
    tableHeaderColor: {
      type: String,
      default: ""
    }
  },
  data() {
    return {
      selected: [],
      users: [
        {
          name: "Mara",
          salary: "38",
          city: "Belgrad"
        },
        {
          name: "Minerva Hooper",
          salary: "$23,738",
          city: "Belgrad"
        },
        {
          name: "Sage Rodriguez",
          salary: "$56,142",
          city: "Belgrad"
        },
        {
          name: "Philip Chaney",
          salary: "$38,735",
          city: "Belgrad"
        },
        {
          name: "Doris Greene",
          salary: "$63,542",
          city: "Belgrad"
        },
        {
          name: "Mason Porter",
          salary: "$78,615",
          city: "Belgrad"
        }
      ]
    };
  }
};
</script>

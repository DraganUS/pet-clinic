<template>
  <div>
    <md-table v-model="users" :table-header-color="tableHeaderColor">
      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="ID">{{ item.id }}</md-table-cell>
        <md-table-cell md-label="Ime">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="Placeno">{{ item.salary }}</md-table-cell>      
        <md-table-cell md-label="Grad">{{ item.city }}</md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "ordered-table",
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
          id: 1,
          name: "Neven Josipovic",
          salary: "36,738",
          city: "Belgrad"
        },
        {
          id: 2,
          name: "Mina Minic",
          salary: "$23,738",
          city: "Novi Sad"
        },
        {
          id: 3,
          name: "Marta Savic",
          salary: "$56,142",
          city: "Zemun"
        },
        {
          id: 4,
          name: "Natasa Natic",
          salary: "$38,735",
          city: "Novi BG"
        }
      ]
    };
  }
};
</script>

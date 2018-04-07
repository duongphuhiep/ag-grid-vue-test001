<template>
  <div>
    <ag-grid-vue :gridOptions="gridOptions"></ag-grid-vue>
  </div>
</template>

<script>
import { AgGridVue } from "ag-grid-vue";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components: {
    "ag-grid-vue": AgGridVue
  },
  data() {
    return {
      gridOptions: {
        rowData: [
          { make: "Toyota", model: "Celica", price: 35000 },
          { make: "Ford", model: "Mondeo", price: 32000 },
          { make: "Porsche", model: "Boxter", price: 72000 }
        ],
        columnDefs: [
          { headerName: "Make", field: "make" },
          { headerName: "Model", field: "model" },
          { headerName: "Price", field: "price" }
        ]
      }
    };
  }
};
</script>

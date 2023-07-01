<script>
import Sidebar from '../components/Sidebar.vue';
import Table from '../components/Table.vue';
export default {
  name: 'TransactionView',
  components: {
    Sidebar,
    Table
  },
  data(){
    return{
      columns: ['Ingredient', 'TotalAmount', 'Unit', 'CostUnit','TotalCost','Supplier'],
      itemsdata:[
        {Ingredient:'oil',TotalAmount:'10',Unit:'ml',CostUnit:'1000',TotalCost:'10000',Supplier:'A'},
        {Ingredient:'water',TotalAmount:'5',Unit:'ml',CostUnit:'1000',TotalCost:'10000',Supplier:'B'},
        {Ingredient:'sugar',TotalAmount:'7',Unit:'g',CostUnit:'1000',TotalCost:'10000',Supplier:'C'},
        {Ingredient:'onion',TotalAmount:'8',Unit:'unit',CostUnit:'1000',TotalCost:'10000',Supplier:'D'},
        {Ingredient:'egg',TotalAmount:'9',Unit:'unit',CostUnit:'1000',TotalCost:'10000',Supplier:'E'},
      ]
    }
  }
}
</script>

<template>
  <main>
    <div>
      <Sidebar />
      <div class="main">
        <div class="head-product">
          <h1>Inventory</h1>
          <button class="btn-add-product">Inventory</button>
        </div>
        <Table :items="itemsdata" :columns="columns" />
      </div>
    </div>
  </main>
</template>

<style scoped>
.main {
  margin-left: 330px;
  width: 75%;
  height: 100%;
  padding: 20px;
}

.head-product {
  display: flex;
  align-items: center;
}

.btn-add-product {
  margin-left: 30px;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: #14213D;
  color: #fff;
  font-size: 16px;
  font-weight: 700;
  cursor: pointer;
}

.btn-add-product:hover {
  background-color: #14213D;
  transform: scale(1.1);
}

</style>
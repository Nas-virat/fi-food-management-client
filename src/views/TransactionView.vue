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
      columns: ['Date','Ingredient', 'Quantity', 'Unit', 'CostUnit','TotalCost','Supplier'],
      itemsdata:[
        {Date:'2021-08-01',Ingredient:'oil',Quantity:'10',Unit:'ml',CostUnit:'1000',TotalCost:'10000',Supplier:'A'},
        {Date:'2022-02-15',Ingredient:'salt',Quantity:'5',Unit:'g',CostUnit:'500',TotalCost:'2500',Supplier:'B'},
        {Date:'2022-06-30',Ingredient:'sugar',Quantity:'2',Unit:'kg',CostUnit:'2000',TotalCost:'4000',Supplier:'C'},
        {Date:'2022-09-10',Ingredient:'flour',Quantity:'3',Unit:'kg',CostUnit:'3000',TotalCost:'9000',Supplier:'D'},
        {Date:'2022-11-25',Ingredient:'milk',Quantity:'1',Unit:'L',CostUnit:'1500',TotalCost:'1500',Supplier:'E'},
        {Date:'2023-01-08',Ingredient:'tomatoes',Quantity:'8',Unit:'pieces',CostUnit:'200',TotalCost:'1600',Supplier:'F'},
        {Date:'2023-04-17',Ingredient:'chicken',Quantity:'2',Unit:'kg',CostUnit:'6000',TotalCost:'12000',Supplier:'G'},
        {Date:'2023-05-29',Ingredient:'onions',Quantity:'3',Unit:'pieces',CostUnit:'100',TotalCost:'300',Supplier:'H'},
        {Date:'2023-07-06',Ingredient:'rice',Quantity:'5',Unit:'kg',CostUnit:'4000',TotalCost:'20000',Supplier:'I'},
        {Date:'2023-09-21',Ingredient:'eggs',Quantity:'12',Unit:'pieces',CostUnit:'500',TotalCost:'6000',Supplier:'J'},
        {Date:'2023-11-08',Ingredient:'garlic',Quantity:'4',Unit:'pieces',CostUnit:'300',TotalCost:'1200',Supplier:'K'},
        {Date:'2024-01-12',Ingredient:'pepper',Quantity:'1',Unit:'g',CostUnit:'100',TotalCost:'100',Supplier:'L'},
        {Date:'2024-03-25',Ingredient:'potatoes',Quantity:'3',Unit:'kg',CostUnit:'1500',TotalCost:'4500',Supplier:'M'},
        {Date:'2024-06-02',Ingredient:'bread',Quantity:'2',Unit:'loaves',CostUnit:'2000',TotalCost:'4000',Supplier:'N'},
        {Date:'2024-08-11',Ingredient:'cheese',Quantity:'500',Unit:'g',CostUnit:'3000',TotalCost:'1500',Supplier:'O'},
        {Date:'2024-10-29',Ingredient:'butter',Quantity:'250',Unit:'g',CostUnit:'2000',TotalCost:'500',Supplier:'P'},
        {Date:'2025-02-14',Ingredient:'cocoa',Quantity:'200',Unit:'g',CostUnit:'1500',TotalCost:'300',Supplier:'Q'},
        {Date:'2025-04-19',Ingredient:'yogurt',Quantity:'1',Unit:'L',CostUnit:'4000',TotalCost:'4000',Supplier:'R'},
        {Date:'2025-07-01',Ingredient:'honey',Quantity:'300',Unit:'ml',CostUnit:'5000',TotalCost:'1500',Supplier:'S'},
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
          <h1>Transaction</h1>
          <button class="btn-add-product">Add Transaction</button>
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
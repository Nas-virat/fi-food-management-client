<script>
import Sidebar from '../components/Sidebar.vue';
import Table from '../components/Table.vue';
import { Bar } from 'vue-chartjs';
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js';
ChartJS.register(BarElement, Title, Tooltip, Legend, CategoryScale, LinearScale);

export default{
  name: 'SaleView',
  components: {
    Sidebar,
    Bar,
    Table,
  },
  data() {
    return {
      chartData: {
        labels: [ 'January', 'February', 'March', 'April', 'May', 'June','July','August','September','October','November','December'],
        datasets: [{
          label: 'Sale',
          data: [40, 20, 12, 20, 30, 52,32,12,43,54,65,76],
          backgroundColor: '#14213D',
          borderWidth: 1,
          barThickness: 20,
          maxBarThickness: 30,
          minBarLength: 2,
        }]
      },
      chartOptions: {
        responsive: true,
      },
      topSale:{
        columns:['name','Quantity','Sale'],
        data:[
          { name: 'Tom Yum Goong', Quantity: '10', Sale: '1000' },
          { name: 'Pad Thai', Quantity: '5', Sale: '500' },
          { name: 'Green Curry', Quantity: '8', Sale: '800' },
          { name: 'Massaman Curry', Quantity: '15', Sale: '1200' },
          { name: 'Som Tum', Quantity: '12', Sale: '1100' },
          { name: 'Khao Pad', Quantity: '7', Sale: '650' },
          { name: 'Panang Curry', Quantity: '9', Sale: '900' },    
        ]
      }
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
          <h1>Sale</h1>
          <button class="btn-add-product">Add Sale</button>
        </div>
        <div class="top-section section">
          <h3>This year Sale</h3>
          <Bar
            id="my-chart-id"
            :options="chartOptions"
            :data="chartData"
          />
        </div>
        <div class="buttom-section ">
          <div class="top-sale section">
            <h3>Top Sale</h3>
            <Table :items="topSale.data" :columns="topSale.columns"/>
          </div>
          <div class="sale-category section">
            <h3>Sale By Category</h3>
          </div>
        </div>
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

.section{
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  border-radius: 5px;
}

.top-section {
  margin-top: 40px;
  padding: 40px;
  display: flex;
  flex-direction: column;
}

.buttom-section {
  margin-top: 40px;
  display: flex;
}

.top-sale {
  width: 50%;
  padding: 20px;
}

.sale-category {
  width: 50%;
  padding: 20px;
}

</style>
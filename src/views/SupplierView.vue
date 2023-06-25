<script>
import Sidebar from '../components/Sidebar.vue';
import Table from '../components/Table.vue';

export default {
  name: 'SupplierView',
  components: {
    Sidebar,
    Table
  },
  data(){
    return{
      itemsdata:[
        {Supplier:'PT. Sinar Jaya',Address:'Jl. Raya Bogor',Phone:'08123456789',Email:'a@gmail.com'},
        {Supplier:'PT. Makmur Sejahtera',Address:'Jl. Sudirman',Phone:'08234567890',Email:'b@gmail.com'},
        {Supplier:'PT. Abadi Sentosa',Address:'Jl. Merdeka',Phone:'08345678901',Email:'c@gmail.com'},
        {Supplier:'PT. Maju Bersama',Address:'Jl. Gatot Subroto',Phone:'08456789012',Email:'d@gmail.com'},
        {Supplier:'PT. Harmoni Indah',Address:'Jl. Thamrin',Phone:'08567890123',Email:'e@gmail.com'},
        {Supplier:'PT. Gemilang Utama',Address:'Jl. Kebon Jeruk',Phone:'08678901234',Email:'f@gmail.com'},
        {Supplier:'PT. Cemerlang Mandiri',Address:'Jl. Tomang',Phone:'08789012345',Email:'g@gmail.com'},
        {Supplier:'PT. Bersatu Abadi',Address:'Jl. Kemanggisan',Phone:'08890123456',Email:'h@gmail.com'},
        {Supplier:'PT. Jaya Makmur',Address:'Jl. Pejaten',Phone:'08901234567',Email:'i@gmail.com'},
        {Supplier:'PT. Sentosa Jaya',Address:'Jl. Puri Indah',Phone:'09012345678',Email:'j@gmail.com'},
        {Supplier:'PT. Indah Makmur',Address:'Jl. Kemang',Phone:'09123456789',Email:'k@gmail.com'},
        {Supplier:'PT. Mulia Sejahtera',Address:'Jl. Menteng',Phone:'09234567890',Email:'l@gmail.com'}
      ],
      columns:['Supplier','Address','Phone','Email']
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
          <h1>Supplier</h1>
          <button class="btn-add-supplier">Add Supplier</button>
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

.btn-add-supplier {
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

.grid-product {
  margin-top: 40px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 20px;
  align-items: center;
}

.card-product {
  width: 100%;
  height: 100%;
  background-color: #fff;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  box-shadow: 0 5px 10px rgba(0,0,0,0.2);
}

.img-product {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 5px;
}

.card-content {
  padding: 20px;
}

.category {
  font-size: 16px;
  font-weight: 300;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.name-product {
  margin-top: 20px;
  font-size: 18px;
  font-weight: 800;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.price-product {
  margin-top: 10px;
  font-size: 16px;
  font-weight: 300;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.stock-product {
  margin-top: 10px;
  font-size: 16px;
  font-weight: 300;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

</style>
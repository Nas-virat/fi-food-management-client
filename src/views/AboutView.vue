<script>
import Sidebar from '../components/Sidebar.vue';
import Table from '../components/Table.vue';

export default{
  name: 'InventoryView',
  components: {
    Sidebar,
    Table,
  },
}
</script>

<template>
  <main>
    <div>
      <Sidebar />
      <div class="main">
        <div class="content">
          <img src="src/assets/img/Fi-icon.png" class="img-food" />
          <br />
          <h2>Find It (FI)</h2>
          <br />
          <p>This project is a personal endeavor that aims to develop a Food Management System specifically designed for small businesses. 
            The primary objective is to enable users to efficiently record sales transactions, track inventory levels, 
            and maintain a comprehensive list of suppliers utilized by the company.
          </p>
          <br />
          <h5>Features:</h5>
          <p>1. Inventory Management</p>
          <p>2. Sales Management</p>
          <p>3. Supplier Management</p>
          <br/>
          <h5>Developed by:</h5>
          <p>Napas Vinitnantharat</p>
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

.head {
  display: flex;
  align-items: center;
}
.img-food {
  width: 250px;
  height: 250px;
  background-color: #fff;
}

.content{
  display: flex;
  align-items: center;
  flex-direction: column;
  margin-top: 50px;
}

p{
  font-size: large;
}

</style>
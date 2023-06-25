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
        <div class="head-product">
          <h1>Inventory</h1>
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
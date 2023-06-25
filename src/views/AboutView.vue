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
        <div class="head">
          <h1>About Us</h1>
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


</style>
<script>
export default {
  data() {
    return {
      productId: null,
      icon: 'src/assets/img/Fi-icon.png',
    };
  },
  created() {
    this.productId = this.$route.params.id;
  },

};
</script>



<template>
    <div class="bg-sidebar">
        <img v-bind:src="icon" class="icon" />
        <div class="list">
            <router-link to="/" class="item">Home</router-link>
            <router-link to="/sales" class="item">Sales</router-link>
            <router-link to="/transaction" class="item">Transaction</router-link>
            <router-link to="/inventory" class="item">Inventory</router-link>
            <router-link to="/supplier" class="item">Supplier</router-link>
            <router-link to="/about" class="item">About Us</router-link>
        </div>
    </div>
</template>


<style scoped>
.bg-sidebar {
    background-color: #000;
    width: 250px;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.icon {
    width: 180px;
    height: 180px;
    background-color: #fff;
}

.list {
    width: 100%;
    margin-top: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.item {
    font-size: 20px;
    font-weight: 700;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;  
    text-decoration: none; 
    color: #fff;
    margin-top: 20px;
    cursor: pointer;
    padding-top: 10px;
}

.item:hover {
    color: #FCA311;
    transform: scale(1.1);
}
</style>
<script setup>

</script>



<template>
    <div class="bg-sidebar">
        <div class="icon"></div>
        <div class="list">
            <div class="item">Home</div>
            <div class="item">Sales</div>
            <div class="item">Transaction</div>
            <div class="item">Inventory</div>
            <div class="item">Supplier</div>
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
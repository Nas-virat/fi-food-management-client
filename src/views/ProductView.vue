<script setup>
import Sidebar from '../components/Sidebar.vue';
</script>


<template>
    <main>
        <div>
            <Sidebar />
            <div class="main">
                <div class="info-food">
                    <div class="header">
                        <h1>Information food</h1>
                        <button class="btn">Edit Product</button>
                    </div>
                    <div class="info-food-content">
                        <img src="src/assets/img/1.jpeg" class="img-food"/>
                        <div class="info-food-text">
                            <div class="category">Category</div>
                            <div class="name-product">Name Product</div>
                            <div class="text-content">Price</div>
                            <div class="text-content">Stock</div>
                            <div class="text-content">Description</div>
                            <div class="text-content">last modify</div>
                        </div>
                    </div>
                </div>
                <div class="ingredient">
                    <div class="header">
                        <h1>Ingredient</h1>
                        <button class="btn">Add Product</button>
                    </div>
                    <div class="ingredient-table">

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

.header{
    display: flex;
    align-items: center;
}

.btn{
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

.btn:hover {
  background-color: #14213D;
  transform: scale(1.1);
}

.info-food-content{
    margin-top: 40px;
    margin-bottom: 40px;
    margin-left: 10px;
    display: flex;
    align-items: center;
}

.img-food {
    width: 400px;
    height: 300px;
    border-radius: 10px;
    margin-right: 80px;
}

.text-content{
    margin-top: 10px;
    font-size: 20px;
    font-weight: 700;
}


</style>
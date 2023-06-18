<script setup>
import Sidebar from '../components/Sidebar.vue';
</script>


<template>
    <main>
        <div>
            <Sidebar />
            <div class="main">
                <div class="info-food">
                    <div class="food-header">
                        <h1>information food</h1>
                        <button class="btn-add-product">Edit Product</button>
                    </div>
                </div>
                <div class="ingredient">
                    <div class="ingredient-header">
                        <h1>ingredient</h1>
                        <button class="btn-add-product">Add Product</button>
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


</style>
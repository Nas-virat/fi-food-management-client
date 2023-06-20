<script>
export default {
    name: 'FoodCard',
    data(){
      return {
        productImage: 'src/assets/img/1.jpeg'
      }
    },
    props:{
      category: {
        type: String,
        required: true
      },
      name: {
          type: String,
          required: true
      },
      price: {
          type: String,
          required: true
      },
      stock: {
          type: String,
          required: true
      }
    },
    methods: {
        navigatorToProduct() {
            this.$router.push(`/product/${1}`)
        }
    }
}
</script>


<template>
    <div class="card-product">
        <img v-bind:src="productImage" class="img-product" />
        <div class="card-content">
            <div class="category">{{ category }}</div>
            <div class="name-product">{{ name }}</div>
            <div class="price-product">{{ price }}</div>
            <div class="stock-product">{{ stock }}</div>
        </div>
        <button class="btn btn-primary" @click="navigatorToProduct">View product</button>
    </div>
</template>

<style scoped>

.card-product {
  width: 100%;
  height: 100%;
  background-color: #fff;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  box-shadow: 0 5px 10px rgba(0,0,0,0.2);
}

.card-product:hover {
  transform: scale(1.1);
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
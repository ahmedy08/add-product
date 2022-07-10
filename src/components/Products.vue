<template>
  <div class="row product-container">
    <product v-for="product in productList">
      <img class="card-img-top" :src="product.selectedImage" :alt="product.name">
      <div class="card-body">
        <h5 class="card-title">{{ product.name }}</h5>
        <small><strong>Adet : </strong> {{ product.piece}}</small>
        <br>
        <small><strong>Fiyat : </strong> {{ product.price }}</small>
        <br>
        <small><strong>Tutar : </strong> {{ product.totalPrice }}</small>
      </div>
    </product>
  </div>
</template>

<script>
import Product from "./Product";
import {eventBus} from "../main";

export default {
  components: {
    Product,
  },
  data() {
    return {
      productList: [],
    }
  },
  created() {
    eventBus.$on("productAdded", (product) =>{
      this.productList.push(product)
    })
  }
}
</script>

<style scoped>

</style>

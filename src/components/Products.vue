<template>
  <div class="row product-container">
    <product v-for="product in productList">
      <img class="card-img-top" src="/src/assets/default.png" alt="Card image cap">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <small><strong>Adet : </strong> 1</small>
        <br>
        <small><strong>Fiyat : </strong> 10</small>
        <br>
        <small><strong>Tutar : </strong> 10</small>
      </div>
    </product>
  </div>
</template>

<script>
import Product from "./Product";

export default {
  components: {
    Product,
  },
  data() {
    return {
      productList: [],
    }
  },
}
</script>

<style scoped>

</style>

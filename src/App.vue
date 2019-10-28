<template>
  <div id="app">
    <my-header></my-header>
    <search-form></search-form>
    <div class="container">
      <products @viewDetails="viewDetails"></products>
      <product-details :product="selectedProduct"></product-details>
  </div>
  </div>
</template>

<script>
import SearchForm from './SearchForm.vue'
import Header from './Header.vue'
import ProductsList from './ProductsList'
import ProductDetails from './ProductDetails'

export default {
  data () {
    return {
      selectedProduct: {}
    }
  },
  components: {
    SearchForm,
    'my-header': Header,
    'products': ProductsList,
    ProductDetails
  },
  methods: {
    viewDetails (product) {
      this.selectedProduct = product
    }
  }
}
</script>

<style>
  .container{
    display:flex;
    align-items:flex-start;
  }
</style>

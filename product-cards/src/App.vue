<template>
  <div id="app">
    <!-- <ul>
      <li v-for="(product, index) in products" :key="product">
        {{ index }}
        {{ product.productId }} 
        {{ product.rating}}

      </li>
    </ul> -->

    <Product :products="products"/>

    
  </div>
</template>

<script>
import Product from './components/Products'


export default {
  name: 'App',

  components: {
    Product

  },

  data(){
    return{
      products: [
        {
          productId: 1063,
          productName: 'lovely brown Theressa',
          productImage: 'https://picsum.photos/400?image=891',
          productStock: 31,
          productPrice: '40426.73',
          productSalePrice: '12936.55',
          rating: 4
        },
        {
          productId: 1068,
          productName: 'primary gold Tera',
          productImage: 'https://picsum.photos/400?image=463',
          productStock: 88,
          productPrice: '25121.63',
          productSalePrice: '25121.63',
          rating: 4
        }
]
    }
  },


  
}
</script>

<style>

</style>

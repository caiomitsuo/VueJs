<template>
  <div id="product-list-one">
    <h2>Product List One</h2>
    <ul>
      <li v-for="product in saleProducts" :key="product">
        <span class="name">{{ product.name }}</span>
        <span class="price">${{ product.price }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  computed: {
    products(){
      return this.$store.state.products
    },
    saleProducts(){
    var saleProducts = this.$store.state.products.map( product => {
      return{
        name:'**' + product.name + '**',
        price:product.price / 2,
      }
    });
      return saleProducts
    }
  }
};
</script>
<style>
#product-list-one {
  background: #fff8b1;
  margin-bottom: 30px;
  padding: 10px 20px;
}
#product-list-one ul {
  padding: 0;
  list-style-type: none;
}

#product-list-one li {
  margin-right: 10px;
  margin-top: 10px;
  padding: 20px;
  background: rgba(255, 255, 255, 0.7);
}
.price {
  font-weight: bold;
  color: #860ce8;
  display: block;
}
</style>

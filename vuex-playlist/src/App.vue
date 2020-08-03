<template>
  <div id="app">
    <product-list-one> </product-list-one>
    <product-list-two> </product-list-two>
  </div>
</template>

<script>
import ProductListOne from "./components/ProductListOne";
import ProductListTwo from "./components/ProductListTwo";

export default {
  components: {
    "product-list-one": ProductListOne,
    "product-list-two": ProductListTwo
  },

  name: "app",
  data() {
    return {};
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@100&display=swap");
body {
  font-family: Roboto;
  color: #555;
}
</style>

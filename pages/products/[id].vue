<template>
  <!-- <div class="container mx-auto p-4">
    <h2>Product details for {{ id }}</h2>
    <p>title: {{ product.title }}</p>
    <p>price: {{ product.price }}</p>
    <p>id: {{ product.id }}</p>
  </div> -->
  <div>
  <ProductDetails :product="product"/></div>
</template>

<script setup>
const { id } = useRoute().params;

const uri = 'https://fakestoreapi.com/products/' + id

//  fetch the product, add unique key to each fetch
const { data: product } = await useFetch(uri, { key: id })

if (!product.value) {
    throw createError({ statusCode: 404, statusMessage: 'Product not found', fatal: true})
  }


definePageMeta({
  layout: "products",
});
</script>

<style scoped></style>

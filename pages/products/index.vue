<template>
    <div class="container mx-auto p-4 ">
   <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products">
        <!-- <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink> -->
        <ProductCard :product="p"/>
        
      </div>
    </div>
  </div>
</template>

<script setup>

definePageMeta({
    layout:'products'
});

  //  fetch the products
  const { data: products } = await useFetch('https://fakestoreapi.com/products')

  //overwrite page title
useHead({
    title: 'Products App | Products',
    meta: [
      { name: 'description', content: 'Products'}
    ]
  })
  

</script>

<style  scoped>

</style>
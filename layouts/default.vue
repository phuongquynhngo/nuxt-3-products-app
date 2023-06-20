<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav  class="container mx-auto p-4 flex justify-between">
        <nuxt-link to="/" class="font-bold">Nuxt Quynh Ngo</nuxt-link>
        <!-- internal links within Nuxt.js apps: avoiding full page reloads,  automatic active class assignment-->
        <ul class="flex gap-4">
          <li><nuxt-link to="/">Home</nuxt-link></li>
          <li><nuxt-link to="/about">About</nuxt-link></li>
          <li><nuxt-link to="/products" class="btn">Products</nuxt-link></li>
          <!-- <li><nuxt-link to="/products/abc" class="btn">abc products</nuxt-link></li> -->
        </ul>
        <!--<a href="/about">normal link to about page</a>
          internal and external links:  full page reloads -->
      </nav>
    </header>
    <!-- output content -->
    <div  class="container mx-auto p-4"><slot /></div>
  </div>
</template>



<style scoped>
  .router-link-exact-active {
    color: #12b488;
  }</style>

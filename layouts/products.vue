<template>
  <div>
    <header class="shadow-sm bg-white">
        <nav class="container mx-auto p-4">
        <nuxt-link to="/products"  class="font-bold">Nuxt Products</nuxt-link>
        <!-- internal links within Nuxt.js apps: avoiding full page reloads,  automatic active class assignment-->

        <!--<a href="/about">normal link to about page</a>
            internal and external links:  full page reloads -->
      </nav>
    </header>
    <!-- output content -->
    <div class="container mx-auto p-4">
      <slot />
    </div>

    <footer class="container mx-auto p-4 flex justify-between border-t-2">
      <ul class="flex gap-4">
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li><nuxt-link to="/about">About</nuxt-link></li>
        <li><nuxt-link to="/products">Products</nuxt-link></li>
      </ul>
    </footer>
  </div>
</template>

<style scoped>
.router-link-exact-active {
  color: #12b488;
}
</style>

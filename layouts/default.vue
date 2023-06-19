<template>
  <div>
    <header>
      <nav>
        <nuxt-link to="/">Nuxt Quynh Ngo</nuxt-link>
        <!-- internal links within Nuxt.js apps: avoiding full page reloads,  automatic active class assignment-->
        <ul>
          <li><nuxt-link to="/">Home</nuxt-link></li>
          <li><nuxt-link to="/about">About</nuxt-link></li>
          <li><nuxt-link to="/products">Products</nuxt-link></li>
        </ul>
        <!--<a href="/about">normal link to about page</a>
          internal and external links:  full page reloads -->
      </nav>
    </header>
    <!-- output content -->
    <div><slot /></div>
  </div>
</template>



<style scoped>
  .router-link-exact-active {
    color: #12b488;
  }</style>

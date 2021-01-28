<template>
  <div>
    <nav class="navbar navbar-dark bg-success">
      <ul class="nav">
        <li class="nav-item active">
          <nuxt-link class="nav-link text-white" to="/">Home</nuxt-link>
        </li>
        <li class="nav-item active">
          <nuxt-link class="nav-link text-white" to="/subscribe">Subscribe</nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link class="nav-link text-white" to="/commandes">Order</nuxt-link>
        </li>
      </ul>
    </nav>
    <Nuxt />
  </div>
</template>

<style scoped>

</style>


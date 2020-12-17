<template>
  <header>
    <h1 class="title">Welcome to the Canteen</h1>
    <ul>
      <li>
        <nuxt-link to="/">Home</nuxt-link>
        <nuxt-link to="/menu">Menu</nuxt-link>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
    </ul>
  </header>
</template>
<script>
export default {
  name: 'AppHeader',
}
</script>

<style scoped></style>

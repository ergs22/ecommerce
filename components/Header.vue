<template>
  <div class="container">
    <nuxt-link to="/" class="container-image">
      <img src="../assets/images/logo-tienda.png" alt="logo" />
    </nuxt-link>
    <div class="options-box">
      <p>Blog</p>
      <p>Contactanos</p>
      <p>Sobre nosotros</p>
    </div>
    <div class="icons-box">
      <img src="../assets/icons/icon-search.svg" alt="icon-search" />
      <img src="../assets/icons/icon-product.svg" alt="icon-product" />
      <img src="../assets/icons/icon-user.svg" alt="icon-user" />
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.container {
  height: 6rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-family: "Manrope", sans-serif;
  width: 90vw;
  margin-left: auto;
  margin-right: auto;
}
.container-image {
  width: 12vw;
}
.container-image img {
  text-decoration: none;
  color: black;
}

.options-box {
  display: flex;
  width: 42vw;
  justify-content: space-around;
  align-items: center;
}

.options-box p {
  cursor: pointer;
}

.icons-box {
  display: flex;
  width: 12vw;
  justify-content: space-around;
  align-items: center;
}
.icons-box img {
  cursor: pointer;
}
</style>

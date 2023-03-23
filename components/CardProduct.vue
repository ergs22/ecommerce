<template>
  <nuxt-link to="/product" class="container">
    <div class="image-container">
      <img src="#" alt="imagen-product" />
    </div>
    <h1>{{ props.name }}</h1>
    <span>{{ props.variant }}</span>
    <p>{{ props.price }}</p>
  </nuxt-link>
</template>

<script setup>
const props = defineProps({
  name: String,
  variant: String,
  price: String,
  image: String,
});
</script>

<style scoped>
.container {
  width: 20vw;
  font-family: "Manrope", sans-serif;
  cursor: pointer;
  text-decoration: none;
  color: black;
}

.image-container {
  background-color: #f8f5ec;
  width: 20vw;
  height: 40vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

h1 {
  font-size: 1.125rem;
  font-weight: 400;
  margin-bottom: 0.4rem;
}
span {
  font-size: 0.875rem;
  font-weight: 400;
  display: inline-block;
}

p {
  font-size: 1.25rem;
  font-weight: 600;
}
</style>

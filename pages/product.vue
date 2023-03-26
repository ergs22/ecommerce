<template>
  <div class="container">
    <Header />
    <div class="container-main">
      <div class="container-image">
        <img :src="dataProduct.image" alt="image-product" />
      </div>
      <div class="container-info">
        <p class="container-info--p-main">
          {{ dataProduct.advertising }}
        </p>
        <h1>{{ dataProduct.name }}</h1>
        <div class="price">
          <h3>{{ dataProduct.price }}</h3>
          <p>
            ({{ dataProduct.stars }} stars) • {{ dataProduct.reviews }} reviews
          </p>
        </div>

        <div class="buttons">
          <div class="box__buttons">
            <button class="button__add-cart">Add to Cart</button>
            <input type="number" name="quantity" id="2" value="1" />
          </div>

          <button class="button__buy-now">Buy now</button>
          <span>Free shipping over $50 </span>
        </div>
      </div>
    </div>

    <div class="container-details"></div>
    <div class="container- similar"></div>
    <Footer />
  </div>
</template>

<script setup>
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
import { onBeforeMount, ref } from "vue";

const dataProduct = ref(null);

onBeforeMount(async () => {
  dataProduct.value = JSON.parse(localStorage.getItem("product"));
});
</script>

<style scoped>
.container {
  font-family: "Manrope";
}
.container-main {
  display: flex;
  width: 88vw;
  overflow-x: hidden;
  padding: 3rem 0;
  justify-content: space-between;
  margin-left: auto;
  margin-right: auto;
}

.container-image {
  width: 44vw;
  height: 100vh;
  background-color: #f8f5ec;
  display: flex;
  align-items: center;
  justify-content: center;
}
.container-info {
  width: 36vw;
  height: 100vh;
}

.container-info .container-info--p-main {
  color: rgba(27, 27, 27, 0.45);
  font-size: 1.25rem;
  font-weight: 400;
  margin-top: 4rem;
}

.container-info h1 {
  font-size: 3rem;
  font-weight: 300;
}

.price {
  display: flex;
  align-items: center;
  margin-bottom: 4rem;
}

.price h3 {
  font-size: 1.5rem;
  font-weight: 300;
  border-right: solid 1px black;
  padding-right: 1rem;
  margin-right: 1rem;
}

.price p {
  font-size: 0.87rem;
  font-weight: 400;
  color: black;
}
.box__buttons {
  display: flex;
  justify-content: space-between;
  margin-bottom: 2rem;
}
.box__buttons .button__add-cart {
  font-weight: 400;
  font-size: 1.3rem;
  color: white;
  padding: 0.9rem 1.5rem;
  background-color: black;
  border: none;
  width: 85%;
  cursor: pointer;
}

.box__buttons input {
  text-align: center;
  font-weight: 400;
  font-size: 1rem;
  width: 10%;
  border: solid black 1px;
}

.buttons .button__buy-now {
  font-weight: 400;
  font-size: 1rem;
  background-color: white;
  padding: 0.9rem 1.5rem;
  border: solid 1px black;
  cursor: pointer;
  width: 100%;
  margin-bottom: 1rem;
}

.buttons span {
  display: inline-block;
  font-weight: 400;
  font-size: 0.75rem;
  width: 100%;
  text-align: center;
}
</style>

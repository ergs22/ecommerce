<template>
  <div>
    <Header />
    <Heroe />
    <Filterbar @showFilter="show" />
    <div v-show="filterOpt">
      <FilterOptions />
    </div>
    <div class="container-products">
      <CardProduct name="Jean Skinny" variant="variant" price="20$" />
      <CardProduct name="Jean Skinny" variant="variant" price="20$" />
      <CardProduct name="Jean Skinny" variant="variant" price="20$" />
      <CardProduct name="Jean Skinny" variant="variant" price="20$" />
      <CardProduct name="Jean Skinny" variant="variant" price="20$" />
      <CardProduct name="Jean Skinny" variant="variant" price="20$" />
      <CardProduct name="Jean Skinny" variant="variant" price="20$" />
      <CardProduct name="Jean Skinny" variant="variant" price="20$" />
    </div>
    <div class="container-showMore">
      <button class="showMore">Mostrar mas...</button>
    </div>
    <Footer />
  </div>
</template>

<script setup>
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
import Heroe from "../components/Heroe.vue";
import Filterbar from "../components/Filterbar.vue";
import FilterOptions from "../components/FilterOptions.vue";
import CardProduct from "../components/CardProduct.vue";
import { ref } from "vue";

const filterOpt = ref(false);

function show(value) {
  filterOpt.value = value;
}
</script>

<style scoped>
.container-products {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding-top: 4rem;
  padding-bottom: 2rem;
  width: 90vw;
  margin-left: auto;
  margin-right: auto;
}
.container-showMore {
  height: 10vh;
  display: flex;
  padding-top: 1rem;

  padding-bottom: 5rem;

  justify-content: center;
  align-items: flex-start;
}

.showMore {
  background-color: transparent;
  border: solid black 1px;
  width: 9vw;
  height: 8vh;
  align-items: center;
  cursor: pointer;
  font-size: 1rem;
  font-weight: 400;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
</style>

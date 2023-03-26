<template>
  <div class="container">
    <div class="container__input">
      <div class="container-text">
        <h3>Buscar</h3>
        <span>clear</span>
      </div>
      <div class="box-input">
        <svg
          @click="searchProduct"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M16.875 15.4554L20.875 19.4602C21.0536 19.6589 21.0448 19.9631 20.855 20.1511L20.155 20.8519C20.0611 20.9467 19.9333 21 19.8 21C19.6667 21 19.5389 20.9467 19.445 20.8519L15.445 16.8471C15.3344 16.7362 15.234 16.6156 15.145 16.4867L14.395 15.4855C13.1541 16.4776 11.613 17.0178 10.025 17.0173C6.75261 17.0287 3.90902 14.7686 3.17773 11.5751C2.44643 8.38161 4.0226 5.10699 6.9731 3.68991C9.92359 2.27284 13.461 3.09151 15.491 5.66125C17.521 8.23099 17.5019 11.866 15.445 14.4142L16.445 15.105C16.6012 15.2051 16.7454 15.3226 16.875 15.4554ZM5.025 10.0089C5.025 12.7736 7.26357 15.0149 10.025 15.0149C11.3511 15.0149 12.6229 14.4875 13.5605 13.5487C14.4982 12.6099 15.025 11.3366 15.025 10.0089C15.025 7.24412 12.7864 5.00285 10.025 5.00285C7.26357 5.00285 5.025 7.24412 5.025 10.0089Z"
            fill="CurrentColor"
          ></path>
        </svg>
        <input
          type="text"
          placeholder="Keyword"
          @keyup.enter="searchProduct"
          v-model="product"
        />
      </div>
    </div>
    <div class="container__input">
      <div class="container-text">
        <h3>Tipo</h3>
        <span>clear</span>
      </div>

      <select name="tipo" id="tipo">
        <option value="Jean">Jean</option>
        <option value="Jean">Jean</option>
        <option value="Jean">Jean</option>
      </select>
    </div>

    <div class="container__input">
      <div class="container-text">
        <h3>Precio</h3>
        <span>clear</span>
      </div>
      <select name="price" id="price">
        <option value="Jean">Jean</option>
        <option value="Jean">Jean</option>
        <option value="Jean">Jean</option>
      </select>
    </div>

    <div class="container__input">
      <div class="container-text">
        <h3>Filtrar cuatro</h3>
        <span>clear</span>
      </div>

      <select name="filterfour" id="filterfour">
        <option value="Jean">Jean</option>
        <option value="Jean">Jean</option>
        <option value="Jean">Jean</option>
      </select>
    </div>
  </div>
</template>

<script setup>
// const props = defineProps({
//   data: Object,

import { ref } from "vue";

// });
const product = ref(null);
const emits = defineEmits(["searchProduct"]);

function searchProduct() {
  emits("searchProduct", product.value);
}
</script>

<style scoped>
.container {
  width: 90vw;
  padding: 2rem 0;
  display: flex;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
.box-input {
  position: relative;
}
.box-input svg {
  position: absolute;
  left: 0.75rem;
  top: 0.75rem;
  cursor: pointer;
}
.container-text {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.container-text h3 {
  font-weight: 400;
  font-size: 1rem;
}
.container-text span {
  font-weight: 400;
  font-size: 0.875rem;
  cursor: pointer;
}

.container__input input {
  width: 20vw;
  min-height: 2.75rem;
  background-color: transparent;
  border: solid 1px #000;
  padding: 0 0 0 2.87rem;
  outline: 0;
}
.container__input select {
  padding: 0.5rem 2.5rem 0.5rem 1rem;
  width: 20vw;
  min-height: 2.85rem;
  background-color: transparent;
  border: solid 1px #000;
  cursor: pointer;
  outline: 0;
}
</style>

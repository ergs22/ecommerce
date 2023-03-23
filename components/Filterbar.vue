<template>
  <div class="container">
    <button @click="showFilter">
      <img src="../assets/icons/icon-filter.svg" alt="icon-filters" /> Filtros
    </button>

    <div class="options">
      <p>Ver todo</p>
      <p>JJeans</p>
      <p>Shorts</p>
      <p>Chaquetas</p>
      <p>Collares</p>
    </div>
    <p>
      Buscar por
      <img src="../assets/icons/icon-down-arrow.png" alt="icon-arrow-down" />
    </p>
  </div>
</template>

<script setup>
import { ref } from "vue";
const emits = defineEmits(["showFilter"]);
const filter = ref(false);
function showFilter() {
  filter.value ? (filter.value = false) : (filter.value = true);
  emits("showFilter", filter.value);
}
</script>

<style scoped>
.container {
  height: 4rem;
  display: flex;
  width: 90vw;
  margin-left: auto;
  margin-right: auto;
  justify-content: space-between;
  align-items: center;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  font-size: 1rem;
  font-weight: 400;
}

.options {
  display: flex;
  width: 30vw;
  justify-content: space-between;
}
p {
  cursor: pointer;
  width: 9vw;
  display: flex;
  align-items: center;
  height: 2rem;
}

p img {
  width: 0.87rem;
  height: 0.87rem;
  margin-left: 0.5rem;
}

button {
  background-color: white;
  border: solid 1px black;
  width: 9vw;
  height: 8vh;
  justify-content: space-evenly;
  display: flex;
  align-items: center;
  cursor: pointer;
}
</style>

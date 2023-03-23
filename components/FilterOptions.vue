<template>
  <div class="container">
    <div class="container__input">
      <div class="container-text">
        <h3>Buscar</h3>
        <span>clear</span>
      </div>
      <input type="text" placeholder="Keyword" />
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
// });
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
  padding: 0 0 0 1rem;
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

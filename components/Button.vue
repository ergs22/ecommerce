<template>
  <button>{{ props.title }}</button>
</template>

<script setup>
const props = defineProps({
  title: String,
});
</script>

<style scoped>
button {
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

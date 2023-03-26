<template>
  <div>
    <Header />
    <Heroe />
    <Filterbar
      @showFilter="show"
      :data="categories"
      @actionsFiltersections="actionsFilter"
    />
    <div v-show="filterOpt">
      <FilterOptions @searchProduct="searchProduct" />
    </div>
    <div class="container-products">
      <template v-for="product in products" v-if="searchActive">
        <CardProduct
          @showProduct="showProduct"
          :name="product.title"
          :subcategory="product.subcategory"
          :variant="product.category"
          :price="product.price"
          :image="product.image"
          v-if="
            product.title.toLowerCase() === ProductName.toLowerCase() ||
            product.title.toLowerCase().includes(ProductName.toLowerCase())
          "
        />
      </template>

      <template v-for="(product, index) in products" v-if="!searchActive">
        <CardProduct
          @showProduct="showProduct"
          :name="product.title"
          :subcategory="product.subcategory"
          :variant="product.category"
          :price="product.price"
          :image="product.image"
          :reviews="product.reviews"
          :stars="product.stars"
          :advertising="product.advertising"
          v-if="
            (product.category.trim() === categoryFilter.trim() ||
              categoryFilter.trim() === 'Ver todos') &&
            index < contPage
          "
        />
      </template>
    </div>
    <div class="container-showMore">
      <button class="showMore" @click="showMore">Mostrar mas...</button>
    </div>
    <Footer />
  </div>
</template>

<script setup>
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
import Heroe from "../components/Heroe.vue";
import Filterbar from "../components/FilterBar.vue";
import FilterOptions from "../components/FilterOptions.vue";
import CardProduct from "../components/CardProduct.vue";
import { ref } from "vue";

import calzadoCaballero from "../assets/images/calzado-caballero.png";
import calzadoDama from "../assets/images/calzado-dama.png";
import calzadoNiño from "../assets/images/calzado-niño.png";
import chemiseCaballero from "../assets/images/chemise-caballero.png";
import chemiseNiño from "../assets/images/chemise-niño.png";
import franelaDama from "../assets/images/franela-dama.png";
import jeanDama from "../assets/images/jean-dama.png";
import pantalonCaballero from "../assets/images/pantalon-caballero.png";
import pantalonNiño from "../assets/images/pantalon-niño.png";
const categoryFilter = ref("Ver todos");
const filterOpt = ref(false);
const searchActive = ref(false);
const ProductName = ref(null);
const contPage = ref(8);
const products = [
  {
    title: "Jean",
    category: "Damas",
    subcategory: "Pantalones",
    price: "10$",
    image: jeanDama,
    reviews: "500",
    stars: "2",
    advertising: "Jean tipo campana, viejas vibras",
  },
  {
    title: "Converse Blanco Dama",
    category: "Damas",
    reviews: "100",
    stars: "3.5",
    advertising: "Excelente calidad y flexibles",
    subcategory: "Calzado",
    price: "14$",
    image: calzadoDama,
  },
  {
    title: "Semi Crop top",
    category: "Damas",
    subcategory: "Camisas",
    price: "8$",
    image: franelaDama,
    reviews: "10000",
    stars: "5",
    advertising: "Crop top alta moda, obtenlo ya!!",
  },

  {
    title: "Joggers De Caballero Basico Capsule Men I",
    category: "Caballeros",
    subcategory: "Pantalones",
    price: "15$",
    reviews: "500",
    stars: "4.5",
    advertising: "Telas importadas de islandia, super comodo",
    image: pantalonCaballero,
  },

  {
    title: "Chemise Uspolo Assn Original Algodon Logo Grande Y Pequeño",
    category: "Caballeros",
    subcategory: "Franelas y Chemises",
    price: "28$",
    image: chemiseCaballero,
    reviews: "50",
    stars: "2.2",
    advertising: "Chemise originales, importadas de EE.UU",
  },

  {
    title: "Zapatos Casuales",
    category: "Caballeros",
    subcategory: "Calzado",
    price: "40$",
    image: calzadoCaballero,
    reviews: "800",
    stars: "3.5",
    advertising: "Para fiestas, el estilo hasta tus pies",
  },

  {
    title: "Zapatos Dep. Escolares Yoyo 16367l Blanco 24-31",
    category: "Niños",
    subcategory: "Calzado",
    price: "16$",
    image: calzadoNiño,
    reviews: "9000",
    stars: "3.5",
    advertising: "Para el comienzo de clases de tus niños",
  },

  {
    title: "Chemise Bombache De Niña Colegial Bambino",
    category: "Niños",
    subcategory: "Franelas y Chemises",
    price: "14$",
    image: chemiseNiño,
    reviews: "10",
    stars: "1",
    advertising: "Excelente calidad y flexibles",
  },

  {
    title: "Pantalón Bambino Tubito Jeans",
    category: "Niños",
    subcategory: "Pantalones",
    price: "5$",
    image: pantalonNiño,
    reviews: "100",
    stars: "3.5",
    advertising: "Skinny jeans, ultima moda",
  },
];

const categories = [
  {
    title: "Ver todos",
  },
  {
    title: "Damas",
    Damas: [
      "Calzado",
      "Blusas",
      "Franelas y Chemises",
      "Camisas",
      "Vestidos",
      "Faldas",
      "Trajes de baño",
      "Pantalones",
      "Shorts",
      "Ropa Interior",
    ],
  },

  {
    title: "Caballeros",
    Caballeros: [
      "Camisas",
      "Pantalones",
      "Shorts",
      "Ropa Interior",
      "Traje de baño",
      "Franelas y Chemises",
      "Calzado",
    ],
  },
  {
    title: "Niños",
    Niños: [
      "Shorts",
      "Calzado",
      "Camisas",
      "Faldas",
      "Franelas y Chemises",
      "Pantalones",
      "Ropa Interior",
      "Traje de baño",
    ],
  },
];

function showMore() {
  if (
    contPage.value < products.length &&
    contPage.value + 8 <= products.length
  ) {
    console.log("entro en el 1");
    contPage.value += 8;
  } else {
    console.log("entro en el 2");

    contPage.value += products.length - contPage.value;
  }
}

function actionsFilter(value) {
  categoryFilter.value = value;
  searchActive.value = false;
}

function showProduct(data) {
  localStorage.setItem("product", JSON.stringify(data));
}

function show(value) {
  filterOpt.value = value;
}

function searchProduct(value) {
  ProductName.value = value;
  searchActive.value = true;
}
</script>

<style scoped>
.container-products {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
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

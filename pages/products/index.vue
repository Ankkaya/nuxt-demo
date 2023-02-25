<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products">
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
definePageMeta({
  layout: "products",
});
type Product = {
  id: number;
  title: string;
  price: number;
  description: string;
  category: string;
  image: string;
};
// fetch the products from the fake store api and store them in the products variable using the useFetch hook from @nuxtjs/composition-api
//
const { data: products } = await useFetch<Product[]>(
  "https://fakestoreapi.com/products"
);

useHead({
  title: "Nuxt Demo | Merch",
  meta: [{ name: "description", content: "Nuxt Demo | Merch" }],
});
</script>

<style scoped></style>

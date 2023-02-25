<template>
  <div>
    <Head>
      <Title>Nuxt Demo | {{ product?.title }}</Title>
      <Meta name="description" :content="product?.description" />
    </Head>
    <ProductDetail :product="product" />
  </div>
</template>

<script setup lang="ts">
type Product = {
  id: number;
  title: string;
  price: number;
  description: string;
  category: string;
  image: string;
};
const { id } = useRoute().params;
const url = `https://fakestoreapi.com/products/${id}`;
const { data: product } = await useFetch<Product>(url, { key: id } as {
  key: string;
});
definePageMeta({
  layout: "products",
});
</script>

<style scoped></style>

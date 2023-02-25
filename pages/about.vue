<template>
  <div>
    <h2>About</h2>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae voluptatum
      sunt hic error? Ratione molestias minus amet, laborum voluptate illo vel
      doloribus accusantium atque, similique reiciendis provident excepturi
      consectetur labore.
    </p>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit aut non
      alias impedit dolorem. Qui facere cupiditate nulla! Officiis neque dicta
      reiciendis ipsa adipisci repudiandae iure sunt facilis non rem!
    </p>
    {{ data }}
  </div>
</template>

<script setup lang="ts">
const { data } = await useFetch("/api/currency/CNY");
</script>

<style scoped>
h2 {
  margin-top: 20px;
  font-size: 36px;
}
p {
  margin: 20px 0;
}
</style>

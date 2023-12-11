<template>
  <p class="text-lg text-red-600">My Grid</p>
  <div class="grid grid-cols-4 gap-4">
    <div v-for="productItem in productList" :key="productItem.id">
      <img
        :src="productItem.image"
        alt="product image"
        class="max-w-4 max-h-4"
      />
      <p class="text-red-500 font-bold">{{ productItem.title }}</p>
      <p>{{ productItem.description }}</p>
    </div>
  </div>
</template>

<script setup>
const { data: productList } = await useFetch(
  "https://fakestoreapi.com/products",
  {
    immediate: true,
    //  baseURL: config.public.apiBase,
    //  method: "POST",
    //  body: {
    //   email: email.value,
    //  },
    lazy: true,
  }
);
console.log(productList.value);
</script>

<style lang="scss" scoped></style>

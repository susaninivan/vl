<template>
  <div class="product-list">
    <myInput v-model="searchText"/>
    {{searchText}}
    <button class="btn btn-outline-success" type="submit">Поиск</button>

            <h1>Список товаров</h1>
                <ul class="d-flex gap-20">
                    <li v-for="(product, index) in products" :key="index">
                        <cardProduct
                        :titel="product.titel"
                        :price="product.price"
                        :count="product.count"
                        :imgUrl="product.imgUrl"
                        @addToCard="addToCard(index, product.titel)"
                        />
                    </li>
                </ul>
  </div>
</template>

<script>
import cardProduct from "./cardProduct.vue";
import myInput from "./myInput.vue";
export default {
  components: { cardProduct, myInput },
  name: "productList",
  data() {
    return {
      searchText: "",
      products: [
        {
          titel: "Заголовок товара",
          price: 1000,
          imgUrl: "https://placehold.jp/286x429.png",
          count: 20,
        },
        {
          titel: "Заголовок товара",
          price: 2000,
          imgUrl: "https://placehold.jp/286x429.png",
          count: 20,
        },
        {
          titel: "Заголовок товара",
          price: 4000,
          imgUrl: "https://placehold.jp/286x429.png",
          count: 20,
        },
        {
          titel: "Заголовок товара",
          price: 1999,
          imgUrl: "https://placehold.jp/286x429.png",
          count: 20,
        },
      ],
    };
  },
  methods: {
    addToCard(index, titel) {
      console.log("Клик на " + `${titel}` + " #" + `${index}`);
    },
  },
};
</script>

<style scoped>
.gap-20 {
  gap: 20px;
}
ul li::marker {
  list-style: none;
}
ul {
  list-style: none;
}
</style>>


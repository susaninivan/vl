<template>
  <div class="card" style="width: 18rem">
    <img :src="imgUrl" class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{ titel }}</h5>
      <p class="card-text">
        Небольшой пример текста, который должен основываться на названии
        карточки и составлять основную часть содержимого карты.
      </p>
      <a @click="addToCard" class="btn btn-primary">Перейти куда-нибудь</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "cardProduct",
  props: {
    titel: {
      type: String,
      // validator(value) {
      //   return value.length < 5;
      // },
    },
    price: Number,
    imgUrl: {
      type: String,
      default: "/img/istockphoto.d09801ef.jpg",
      requert: true,
    },
    count: {
      type: Number,
      default: 0,
    },
  },
  methods: {
    addToCard() {
      this.$emit("addToCard");
    },
  },
};
</script>

<style>
</style>

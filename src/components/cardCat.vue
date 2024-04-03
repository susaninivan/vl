<template>
  <div class="card" style="width: 18rem">
    <img
      v-if="isCatVisible"
      src="../assets/istockphoto.jpg"
      class="card-img-top"
      alt="..."
      v-bind:class="imgFilters "
    />
    <p vi-else>Кот скоро появится</p>
    <div class="card-body">
      <h5 class="card-title">Заголовок карточки</h5>
      <p class="card-text">
        Небольшой пример текста, который должен основываться на названии
        карточки и составлять основную часть содержимого карты.
      </p>
      <a @click="isCatVisible = !isCatVisible" href="/" class="btn btn-primary"
        >Перейти куда-нибудь</a
      >
      <a @click="imgFilters.sepia = !imgFilters.sepia" href="#" class="btn btn-primary"
        >Sepia</a
      >
     <a @click="imgFilters.border = !imgFilters.border" href="#" class="btn btn-primary"
        >border</a
      >
     <a @click="imgFilters.small = !imgFilters.small" href="#" class="btn btn-primary"
        >small</a
      >
     
    </div>
  </div>
</template>

<script>
export default {
  name: "cardCat",

  data() {
    return {
      isCatVisible: true,
      imgFilters: {
        sepia: false,
        border: false,
        small: false,
      },
    };
  },
};
</script>

<style scoped>
img {
  transition: 0.2s ease;
}
img.sepia {
  filter: sepia(100%);
}
img.border {
  border: 2px dashed rgb(185, 15, 0);
}
img.small {
  width: 50%;
}
</style>
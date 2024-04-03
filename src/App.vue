<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

  <div id="app2" class="container">
    <div class="row">
      <div class="col"><my-component /></div>
    </div>
    <div class="row">
      <div class="col-4"><email-component /></div>
      <!-- <div class="col-8">col-8</div>
    <div class="col-4">col-4</div> -->
      <div class="col-8">
        <userCard />
      </div>
    </div>

    <div class="row">
      <div class="col-4">
        <cardCat />
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        <cardCat />
        <productList />
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        <photoRedactor />
      </div>
    </div>
    <div class="row">
      <div class="col-8">
        <singUp/>
      </div>
    </div>
  </div>
</template>

<script>
import userCard from "./components/userCard.vue";
import EmailComponent from "./components/EmailComponent.vue";
import MyComponent from "./components/MyComponent.vue";
// import HelloWorld from './components/HelloWorld.vue'
import cardCat from "./components/cardCat.vue";
// import cardProduct from "./components/cardProduct.vue"
import productList from "./components/productList.vue";
import photoRedactor from "./components/photoRedactor.vue";
import singUp from "./components/singUp.vue";

export default {
  name: "App",
  components: {
    MyComponent,
    EmailComponent,
    userCard,
    cardCat,
    // cardProduct,
    productList,
    photoRedactor,
    singUp,
  },
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>

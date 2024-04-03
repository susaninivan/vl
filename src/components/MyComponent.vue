<template>
  <div class="app3">
    {{ text }}
    <span 
    :class="iconHome">   
    </span>
  
  </div>
</template>

<script>

export default {
  name: "MyComponent",
  data() {
    return {
      text: "HelloWorld",
      iconHome: "material-symbols-outlined",
    };
  },
  mathode: {},

  // computed: {
  //   setClass() {
  //       console.log("1")
  //     return this.iconHome;
      
  //   },
  // },
};
</script>

<style>
</style>
<script>
  import { myCards } from '../assets/data/db'
  import ProductCardVue from '../components/partials/ProductCard.vue'
  // import ProductCardVue from './partials/ProductCard.vue'


export default{
  components:{
    ProductCardVue
  }
}

</script>


<template>

<main class="dritto">
  <div class="container">

    <ProductCardVue />

  </div>
</main>

</template>

<style lang="scss" scoped>

@use '../assets/scss/main.scss';

  main{

  .h2{
    margin-bottom: 30px;
  }
  .container{
    display: flex;
    flex-wrap: wrap;
  }
  }

</style>
<script>
  import { myCards } from '../../assets/data/db';

  export default{
    data(){
      return{
        myCards
      }
    },
    computed:{
        cardCycle() {
        return (this.myCards.products);
      }
    }


  }


</script>


<template>
  <section 
  v-for="(item, index) in cardCycle" 
  :key="index" 
  class="container-card">
    <div class="card-relaxed">
      <img :src="item.frontImage" alt="">
    </div>
    <div class="text relaxed">
      <span class="brand">{{ item.brand }} </span>
      <h1 class="clothes-name">{{ item.name }}</h1>
      <span class="solded-price">{{ item.soldedPrice }} &euro;</span>
      <span class="original-price">{{ item.originalPrice }} &euro;</span>
    </div>
  </section>
</template>




<style lang="scss" scoped>

  @use '../../assets/scss/main.scss';

  .container-card{
    width: 400px;
    height: 700px;
    margin: 10px;
    position: relative;
    color: black;
  }

</style>
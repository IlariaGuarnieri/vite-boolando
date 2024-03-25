<script>
  import { myCards } from '../../assets/data/db';

  export default{
    data(){
      return{
        myCards
      }
    },
    // non lo uso perche le img sono in public e non in src (collegato a riga 34)
    // methods:{
    //   getImagePath(image){
    //     return new URL(`../../../public/img/${image}`, import.meta.url).href;
    //   }
    // },
    computed:{
        cardCycle() {
        return (this.myCards.products);
      },
      discountPrice(){
        let discountExist = false;
        let discount;
        let priceDiscount;
        this.CardObj.badges.forEach(b=>{
          if(b.type =='discount'){

          }
        })
      }
    }
  }

</script>


<template>
  <section 
  v-for="(item, index) in cardCycle" 
  :key="index" 
  class="container-card">
  
    <div>
      <img class="product-levis" :src="`/img/${item.frontImage}`" alt="immagine prodotto">
      <!-- // non lo uso perche le img sono in public e non in src (collegato a riga 10) -->
      <!-- <img :src="getImagePath(item.frontImage)" alt="immagine prodotto"> -->
      <img class="product-levis" id="levis-none" :src="`/img/${item.backImage}`" alt="immagine prodotto">
    </div>
    <div class="text relaxed">
      <span class="brand">{{ item.brand }} </span>
      <span class="hearts">&hearts;</span>
        <div class="sconto">{{item.badges.value}}</div>
        <div class="sostenibilità"> Sostenibilità</div>
      <h1 class="clothes-name">{{ item.name }}</h1>
      <span class="solded-price">{{ item.price }} &euro;</span>
      <span class="original-price">{{ item.originalPrice }} </span>
    </div>
  </section>
</template>




<style lang="scss" scoped>

  @use '../../assets/scss/main.scss';



  .container-card{
    width: 300px;
    height: 600px;
    margin: 10px;
    position: relative;
    color: black;
    .img-fronte:hover{
      display:block;
    }
  }

  .product-levis{
  width: 300px;
  height: 500px;
  margin: 5px;
}
  #levis-none{
  display: none;
}

.product:hover #levis-none{
  display: block;
}

.product:hover .product-levis{
  display: none;
}

.sconto{
  position: absolute;
  top: 450px;
  left:40px ;
  background-color: red;
  color: white;
}

.sostenibilità{
  position: absolute;
  top: 450px;
  left: 80px;
  background-color: green;
  color: white;
}

.hearts{
  font-size: 30px;
  position: absolute;
  left: 310px;
  top: 20px;
  background-color: white;
  width: 40px;
}

</style>
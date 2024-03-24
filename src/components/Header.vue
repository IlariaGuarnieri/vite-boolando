<script>
  export default{
    
    data() {
      return {
        immagine: 'boolean-logo.png'
      }
    },

    methods: {
      getImagePath(image){
        return new URL(`../assets/img/${image}`, import.meta.url).href;
      },
    },
  }
</script>

<template>

  <header class="dritto">
        <section class="container header">
          <div class="options">
            <!-- <ul>
              <li> Donna</li>
              <li>Uomo</li>
              <li>Bambino</li>
            </ul> -->
            <span>Donna</span>
            <span>Uomo</span>
            <span>Bambino</span>
          </div>
    
          <div class="small-logo">
            <img class="logo" :src="getImagePath(immagine)" alt="logo">
          </div>
    
          <div class="col">
      <nav>
        <ul class="social-menu">
          <span><i class="fa-regular fa-user"></i></span>
          <span><i class="fa-regular fa-heart"></i></span>
          <span><i class="fa-regular fa-bag-shopping"></i></span>
        </ul>
      </nav>
    </div>
        </section>
      </header>

</template>


<style lang="scss" scoped>

@use '../assets/scss/main.scss';

header{
  height: 80px;
  background-color: rgba(255,105,0,255);

    .container.header{
      display: flex;
      align-items: center;
      justify-content: space-between;
      max-height: 100%;
      
      .options{
      padding-right: 10px;
        span{
          font-size: 1rem;
          padding: 10px;
          
          &:hover{
            text-decoration: underline;
          }
        }
      } 
      .small-logo{
        max-width: 40%;
        max-height: 70%;

      .logo{
        width: 40%;
        height: 50%;
      }
    }
  }
}

span .fa-regular{
  padding: 10px;
  &:hover{
    text-decoration: underline;
    }
}

</style>
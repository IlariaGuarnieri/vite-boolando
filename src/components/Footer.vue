<script>

</script>


<template>
  <footer class="container">
    <div>
      <h4>Boolando s.r.l.</h4>
      <ul>
        <li><a href="#">Info legali</a></li>
        <li><a href="#">Info privacy</a></li>
        <li><a href="#">Diritto recesso</a></li>
      </ul>
    </div>
    <h5>trovaci anche su</h5>
    <ul class="social-networks">
      <li>
        <a href="#"> <i class="fa-brands fa-twitter-square"></i></a>
      </li>
      <li>
        <a href="#"> <i class="fa-brands fa-facebook-square"></i></a>
      </li>
      <li>
        <a href="#"> <i class="fa-brands fa-instagram-square"></i></a>
      </li>
      <li>
        <a href="#"> <i class="fa-brands fa-youtube-square"></i></a>
      </li>
      <li>
        <a href="#"> <i class="fa-brands fa-pinterest-square"></i></a>
      </li>
    </ul>
  </footer>
</template>


<style lang="scss" scoped>

  @import '../assets/scss/main.scss';

  footer{
    color:white;
    background-color: #1a1a1a;
    padding: 10px 0;
    .container{
      display: flex;
      padding: 20px 10px;
      align-items: flex-start;
      justify-content: space-between;
    }
    .social-networks{
        font-size: 21px;
      }
      ul{
        display: flex;
        list-style-type: none ;
        li{
          margin-right: 10px;
          list-style-type: none ;
          a{

            color : white;
            text-decoration: none;
          }
          &:hover{
            text-decoration: underline;
          }
        }
      }
  }

  // footer{
  //   height: 100px;
  //   background-color: black;
  //   color: white;
  // }

</style>
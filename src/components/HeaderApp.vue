<template>
  <div class="container-fluid p-0 ">
      <!-- section about  -->
      <div class="about d-flex  align-items-center">
        <h3>Everything about Lifestyle, Travel and Gadgets!</h3>
        <a href="#">SIGN IN</a>
        <a href="#">ABOUT US</a>
        <a href="#">CONTACT US</a>
        <a href="#">BUY NOW</a>
      </div>
      <!-- section logo  -->
      <div class="logo d-flex align-items-center">
        <img src="../assets/img/logo-default-slim.png" alt="">
        
      </div>
      <!-- nav bar  -->
       <hr>
      <nav class="navbar">
       
        <div  v-for="(bar,index) in dati" :key="index">
          <a href="#">{{bar}}</a>
        </div>
      </nav>
  </div>
</template>

<script>
import header from '../header.json'
export default {
  name:'HeaderApp',
  data(){
    return{
      dati: header,

    }
    },
    methods:{
       
       
    },
    computed:{

    },
}
</script>

<style lang="scss" scoped>
@import "./style/general.scss";
  .about{
    height: 5vh;
    background-color: $bg-blue;
    h3{
      margin-left: 10%;
      color: $txt-white;
      font-size: 0.8rem;
      margin-bottom: 0; 
    }
    a{
      text-decoration: none;
      color: $txt-white;
      font-size: 0.9rem;
      margin-left: 15px;
      font-weight: 4200;
    }
  }
  .logo{
    height: 12vh;
    width: 80%;
    margin: 0 auto;
    background-color: $bg-white;
    img{
      height: 50%;
    }
  }
  hr{
      background-color:$bg-grey-white ;
      margin: 0 !important;

    }
  .navbar{
    height: 6vh;
    width: 50%;
    margin-left: 10%;
    background-color: $bg-white;
    a{
      text-decoration: none;
      color: $txt-black;
      font-weight: 700;
      &:hover {
        color: $txt-blue;
      }
      &:active {
        color: $txt-blue;
      }
    }
  }


</style>
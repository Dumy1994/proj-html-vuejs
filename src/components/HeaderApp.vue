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
        <img class="img-logo" src="../assets/img/logo-default-slim.png" alt="">
        
      </div>
      <!-- nav bar  -->
       <hr>
      <nav class="navbar d-flex">
       <div class="d-flex">
          <div class=""  v-for="(bar,index) in dati" :key="index">
            <a :class="{'active' : !index} " href="#">{{bar}}</a>
          </div>
       </div>
        
        <div class=" lent float-end">
          <i v-on:click="seen = !seen" class="fa-solid fa-magnifying-glass"></i>
          <div v-if="seen" class="search d-flex justify-content-center align-items-center">
            
            <div class="input-search">
              <input type="text"  placeholder="Type and hit enter ..."  >
            </div>
            <div v-on:click="seen = !seen" class="close">
              <i class="fa-solid fa-xmark"></i>
            </div>
          </div>
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
      seen: !true
    }
    },
    methods:{
       
       
    },
    computed:{

    },
}
</script>

<style lang="scss" scoped>
@import "./style/variables.scss";

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
      font-size: 0.7rem;
      margin-left: 15px;
      font-weight: 4200;
      &:hover{
        color: $txt-grey-white;
      }
    }
  }
  .logo{
    height: 12vh;
    width: 100%;
    margin: 0 ;
    .img-logo{
      animation: logo 15s ease infinite;
      position: relative;
      @keyframes logo {
      from {left: 10%;}
      to {left: 80%;}
    }
    }
    
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
    width: 80%;
    margin-left: 10%;
    
    a{
      font-size: 0.9rem;
      margin-right: 40px;
      text-decoration: none;
      color: $txt-black;
      font-weight: 600;
      &:hover {
        color: $txt-blue;
      }
    }
    .active {
        color: $txt-blue;
      }
  }
  .lent{
    z-index: 1000;
    cursor: pointer;
    
    .search{
      position: absolute;
      left: 0;
      top: 0;
      z-index: 100;
      height: 70vh;
      width: 100%;
      background-color: $bg-white1;
      color: $txt-white;
      .close{
        position: absolute;
        top: 10px;
        right: 10px;
        font-size: 2rem;
        color: $txt-blue;
      }
      .input-search{
        input{
          width: 150%;
          background-color: $bg-trasparent;
          color: $txt-blue;
          border-top: none;
          border-right: none;
          border-left: 2px solid $txt-blue;
          border-bottom: 2px solid $txt-blue;
        }

      }
    }
           
  }
::placeholder {
  color: $txt-blue;
  padding: 10px;
  }
</style>
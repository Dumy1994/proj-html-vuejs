<template>
  <div class="container-fluid p-0">
    <div class="container-footer d-flex ">
      <div class="triangle"></div>
      <div class="get-in-touch">
        <h3>Get in Touch</h3>
      </div>
      <!-- ABOUT THE BLOG  -->
      <div class="col-4 about ">
        <h2>ABOUT THE BLOG</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec eu pulvinar magna semper scelerisque.
        </p>
        <p>Praesent venenatis turpis vitae purus semper, eget sagittis velit venenatis ptent taciti sociosqu ad litora..</p>
        <a href="#">VIEW MORE<i class="fa-solid fa-angle-right"></i></a>
      </div>
      <!-- RECENT POSTS  -->
      <div class="col-3 recent-posts ">
        <h2>RECENT POSTS</h2>
        <div class="pc d-flex">
          <img src="../assets/img/our-office-4-square.jpg" alt="office">
          <div class="d-flex flex-column align-self-center">
            <h3>Lorem ipsum dolor sit, consectetur adipiscing elit</h3>
            <h4>12:53 AM Dec 19th</h4>
          </div>
        </div>
        <div class="kitchen d-flex">
          <img src="../assets/img/our-office-5-square.jpg" alt="office">
          <div class="d-flex flex-column align-self-center">
            <h3>Lorem ipsum dolor sit, consectetur adipiscing elit</h3>
            <h4>12:53 AM Dec 19th</h4>
          </div>
          
        </div>
      </div>
      <!-- recent-comments  -->
      <div class="col-3 recent-comments ">
        <h2>RECENT COMMENTS</h2>
        <div class="comments">
          <h3><i class="fa-solid fa-angle-right"></i><strong>John Doe</strong> commented on 
          <a href="#">lorem ipsum dolor sit amet.</a></h3>
          <h4>12:55 AM Dec 19th</h4>
        </div>
        <div class="comments">
          <h3><i class="fa-solid fa-angle-right"></i><strong>John Doe</strong> commented on  
          <a href="#">lorem ipsum dolor sit amet.</a></h3>
          <h4>12:55 AM Dec 19th</h4>
        </div>
      </div>
      <!-- CATEGORIES  -->
      <div class="col-2 categories-container ">
        <h2>CATEGORIES</h2>
          <div class="float-start categories" v-for="(cat,index) in categories" :key="index">
            <a href="#">{{cat}}</a>
        </div>
      </div>
    </div>
    <!-- footer-section2  -->
    <div class="footer-section2">
      <div class="container-footer d-flex">
        <div class="col-6 d-flex porto-logo align-items-center">
          <img src="../assets/img/logo-footer.png" alt="">
          <h4> Copyright 2020. All Rights Reserved.</h4>
        </div>
        <div class="col-6 porto-logo  d-flex justify-content-end">
          <h4><i class="fa-solid fa-angle-right"></i>FAQ's</h4>
          <h4><i class="fa-solid fa-angle-right"></i>Sitemap</h4>
          <h4><i class="fa-solid fa-angle-right"></i>CONTACT Us</h4>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
    name:'FooterApp',
    data(){
        return{
            categories: ['GADGETS','PHOTOGRAPHY','LIFESTYLE','FASHION','RECIPES','TRAVEL','BUSINESS','ARCHITECTURE','REVIEWS','SPORTS','VIDEOS','TECHNOLOGY','DESIGN']
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
  .container-fluid{
    background-color: $bg-black2;
  }
  .container-footer{
    width: 80%;
    margin: 0 auto;
    position: relative;
    .triangle{
      width: 0;
      height: 0;
      border-left: 10px solid transparent;
      border-bottom: 20px solid $bg-blue-dark;
      z-index: 1000;
      position: absolute;
      top: -20px;
      left: -10px;
    }
    .get-in-touch{
      height: 40px;
      background-color: $bg-blue;
      color: $txt-white;
      position: absolute;
      top: -20px;
      
      h3{
        margin-left: 10px;
        margin-right: 10px;
        line-height: 40px;
        font-style: italic;
        font-size: 1rem;
      }
      
    }
    
    .about{
      margin-top: 70px;
      h2{
        color: $txt-white;
      }
      h3{
        font-weight: 600;
         color: $txt-grey;
      }
      p{
         color: $txt-grey;
      }
      a{
        text-decoration: none;
        color: $txt-white;
        i{
          margin-left: 5px;
        }
      }
    }
    .recent-posts{
      margin-top: 70px;
      h2{
          color: $txt-white;
        }
      .pc{
        margin-bottom: 20px;
        img{
          border-radius: 50%;
          width: 60px;
          height: 60px;
          margin-right: 20px;
        }
        
        h3{
          color: $txt-white;
          font-weight: 300;
          }
          h4{
            color: $txt-grey;
          }
      }
      .kitchen{
        img{
          border-radius: 50%;
          width: 60px;
          height: 60px;
          margin-right: 20px;
        }
        h3{
            color: $txt-white;
            font-weight: 300;
        }
        h4{
          color: $txt-grey
        
        }
      }
    }
    .recent-comments{
      margin-top: 70px;
      .comments{
        margin-bottom: 30px;
        h3{
          color: $txt-white;
          i{
            color: $txt-blue;
            margin-right: 10px;
          }
          a{
            text-decoration: none;
            color: $txt-blue;
          }
        }
        h4{
          color: $txt-grey;
        }
      }
    }
    .categories-container{
      margin-top: 70px;
      h2{
        color: $txt-white;
        padding-left: 5px;
      }
      .categories{
        margin-left: 10px;
        background-color: $bg-black;
        margin-top: 6px;
        border-radius: 6px;
        a{
          text-decoration: none;
          color: $txt-white;
          padding-left: 5px;
          padding-right: 5px;
          font-size: 0.7rem;
          
        }
      }
      
    }
  }
  .footer-section2{
    height: 70px;
    width: 100%;
    background-color: $bg-black3;
    margin-top: 50px;
    
    .container-footer{
      width: 80%;
      margin: 0 auto;
      .porto-logo{
        
        img{
          height: 35px;
          opacity: 60%;
          line-height: 70px;
        }
        h4{
          color: $txt-grey;
          margin-left: 20px;
          line-height: 70px;
          i{
            margin-right: 5px;
          }
        }
      }
    }
  }
</style>
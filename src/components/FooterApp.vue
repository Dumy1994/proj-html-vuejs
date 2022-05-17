<template>
  <div class="container-fluid p-0">
    <div class="container-footer d-flex debug">
      <!-- ABOUT THE BLOG  -->
      <div class="col-4 about debug">
        <h2>ABOUT THE BLOG</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec eu pulvinar magna semper scelerisque.
        </p>
        <p>Praesent venenatis turpis vitae purus semper, eget sagittis velit venenatis ptent taciti sociosqu ad litora..</p>
        <a href="#">VIEW MORE</a>
      </div>
      <!-- RECENT POSTS  -->
      <div class="col-3 recent-posts debug">
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
      <div class="col-3 recent-comments debug">

      </div>
      <div class="col-2 categories debug">

      </div>
    </div>
  </div>
</template>

<script>
export default {
    name:'FooterApp',
    data(){
        return{
            
        }
    },
    methods:{
       
       
    },
    computed:{

    },
}
</script>

<style lang="scss" scoped>
  .container-footer{
    width: 80%;
    margin: 0 auto;
    .about{
      min-height: 100px;
      h3{
        font-weight: 600;
      }
      p{

      }
      a{
        text-decoration: none;
      }
    }
    .recent-posts{
min-height: 100px;
      .pc{
        img{
          border-radius: 50%;
        }
      }
      .kitchen{
        img{
          border-radius: 50%;
          h3{

          }
          h4{

          }
        }
      }
    }
    .recent-comments{
min-height: 100px;
    }
    .categories{
min-height: 100px;
    }
  }
</style>
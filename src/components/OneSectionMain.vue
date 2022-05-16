<template>
  <div class="p-0 container-fluid section">
      <div class="preview d-flex flex-column justify-content-between">
          <!-- section 1  -->
          <div class="col-12 container-card d-flex justify-content-between">
              <div class="col-3 card ">
                  <img src="../assets/img/blog-46.jpg" alt= "blog-46">
              </div>
              <div class="col-3 card  ">
                  <img src="../assets/img/blog-47.jpg" alt= "blog-47">
              </div>
              <div class="col-3 card ">
                  <img src="../assets/img/blog-48.jpg" alt= "blog-48">
              </div>
          </div>
          <!-- section 2  -->
          <div class="col-12 container-card d-flex justify-content-between">
              <div class="col-3 card ">
                  <img src="../assets/img/blog-49.jpg" alt= "blog-49">
              </div>
              <div class="col-3 card  ">
                  <img src="../assets/img/blog-50.jpg" alt= "blog-50">
              </div>
              <div class="col-3 card ">
                  <img src="../assets/img/blog-51.jpg" alt= "blog-51">
              </div>
          </div>

         

      </div>
  </div>
</template>

<script>
export default {
  name:'OneSectionMain',
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

<style lang="scss">
@import "./style/general.scss";
.section{
    background-color: $bg-white-dark;
    .preview{
    width: 80%;
    margin-top: 20px !important;
    margin: auto;
    
    .container-card{
        
        .card{
            width: 32%;
            margin-bottom: 20px ;
            img{
                width: 100%;
                object-fit: contain;
            }
        }
    }
}
}


</style>

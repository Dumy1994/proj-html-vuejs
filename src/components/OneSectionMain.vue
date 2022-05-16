<template>
  <div class="debug p-0 container-fluid section">
      <div class="preview d-flex flex-column justify-content-between  debug2">
          <!-- section 1  -->
          <div class="col-12 container-card d-flex justify-content-between debug">
              <div class="col-3 card debug2">
                  <img src="../assets/img/blog-46.jpg" alt= "blog-46">
              </div>
              <div class="col-3 card  debug2">

              </div>
              <div class="col-3 card debug2">

              </div>
          </div>
          <!-- section 2  -->
          <div class="col-12 container-card d-flex justify-content-between debug">
              <div class="col-3 card debug2">

              </div>
              <div class="col-3 card  debug2">

              </div>
              <div class="col-3 card debug2">

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
    height: 45vh;
    margin: 5vh auto;
    
    .container-card{
        height: 20vh;
        .card{
            width: 31%;
            img{
                height: 100%;
            }
        }
    }
}
}


</style>

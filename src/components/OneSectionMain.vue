<template>
  <div class="p-0 container-fluid section">
    <div class="preview d-flex flex-column justify-content-between">
        <!-- section 1  -->
        <div class="col-12 container-card d-flex justify-content-between sec-1 margin-top">
            <div class="col-3  card ">
                <img src="../assets/img/blog-46.jpg" alt= "blog-46">
                <div class="title">
                    <span class="name">
                        PHOTOGRAPHY
                    </span>
                    <div class="info">
                        How To Take Better Concert Pictures in 30
                        Seconds
                    </div>
                </div>   
            </div>
            <div class="col-3 card  ">
                <img src="../assets/img/blog-47.jpg" alt= "blog-47">
                <div class="title">
                    <span class="name">
                        GADGETS
                    </span>
                    <div class="info">
                        Gadgets That Make Your Smartphone
                        Even Smarter
                    </div>
                </div> 
            </div>
            <div class="col-3 card ">
                <img src="../assets/img/blog-48.jpg" alt= "blog-48">
                <div class="title">
                    <span class="name">
                        TRAVEL
                    </span>
                    <div class="info">
                        20 Top-Rated Tourist Attractions in
                        Manhattan
                    </div>
                </div> 
            </div>
        </div>
          <!-- section 2  -->
        <div class="col-12 container-card d-flex justify-content-between">
            <div class="col-3 card ">
                <img src="../assets/img/blog-49.jpg" alt= "blog-49">
                <div class="title">
                    <span class="name">
                        LIFESTYLE
                    </span>
                    <div class="info">
                        The Best Way to Ride a Motorcycle
                    </div>
                </div> 
            </div>
            <div class="col-3 card  ">
                <img src="../assets/img/blog-50.jpg" alt= "blog-50">
                <div class="title">
                    <span class="name">
                        TRAVEL
                    </span>
                    <div class="info">
                        5 Fun Things to Do at the Beach
                    </div>
                </div> 
            </div>
            <div class="col-3 card ">
                <img src="../assets/img/blog-51.jpg" alt= "blog-51">
                <div class="title">
                    <span class="name">
                        RECIPES
                    </span>
                    <div class="info">
                        Amazingly Fresh Fruit And Herb Drinks For
                        Summer
                    </div>
                </div> 
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

<style lang="scss" scoped>
@import "./style/general.scss";
.section{
    background-color: $bg-white-dark;
    .preview{
    width: 80%;
    margin: auto;
    .margin-top{
        margin-top: 20px;
    }
    .container-card{
        
        .card{
            width: 32%;
            margin-bottom: 20px ;
            position: relative;
            img{
                width: 100%;
                object-fit: contain;
            }
            .title{
                position: absolute;
                    left: 20px;
                    bottom: 20px;
                    max-width: 90%;
                .name{
                    color: $txt-white;
                    padding: 3px;
                    font-weight: 650;
                    font-size: 0.8rem;
                    background-color: $bg-blue;
                 }
                .info{
                    font-weight: 650;
                    color: $txt-white;
                }
            }
        }
    }
}
}


</style>

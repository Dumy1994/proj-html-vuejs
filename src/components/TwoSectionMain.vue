<template>
  <section class="container-fluid p-0 debug">
    <div class=" container-section d-flex justify-content-between">
        <div class="section d-flex flex-column debug2">
            <h2>
                POPULAR POSTS
            </h2>
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../assets/img/blog-55.jpg" alt="blog-55">
                    <span>
                        <h3>Simple Ways to Have a Pretty Face</h3>
                        <h4>Januory 12, 2019</h4>
                    </span>
                </div>
                <hr>  
            </div>
        </div>
        <div class="section debug2">

        </div>
        <div class="section debug2">

        </div>
    </div>

  </section>
</template>

<script>
export default {
    name: 'TwoSectionMain',
    data(){
        return{

        }
    }
}
</script>

<style lang="scss" scoped>
@import "./style/general.scss";
    section{
        min-height: 50vh;
        
        .container-section{

            width: 80%;
            margin: 20px auto;
            .section{
                width: 30%;
                min-height: 50vh;
                .popular{
                    .section-popular{
                        
                        img{
                            width: 50px; 
                        }
                        span{
                            
                            h3{
                                color: $txt-grey2;
                                font-weight: 400;
                                margin-left: 10px;
                            }
                            h4{
                                color: $txt-grey-white;
                                margin-left: 10px;
                            }
                        }
                        
                    }
                    hr{
                        color:red;
                    }
                    
                    
                }
            }
        }
        
    }
</style>

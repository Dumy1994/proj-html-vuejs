<template>
        <div class="section d-flex flex-column ">
            <h2>
                RECENT POSTS
            </h2>
             <!-- section 1  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-65.jpg" alt="blog-65">
                    <span>
                        <h3>Main Reasons To Stop Texting And Driving</h3>
                        <h4>January 12, 2019</h4>
                    </span>
                </div>
                <hr>  
            </div>
            <!-- section 2  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-66 (1).jpg" alt="blog-66">
                    <span>
                        <h3>Tips to Help You Quickly Prepare your Lunch</h3>
                        <h4>January 12, 2019</h4>
                    </span>
                </div>
                <hr>  
            </div>
            <!-- section 3  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-67.jpg" alt="blog-67">
                    <span>
                        <h3>Why should I buy a smartwatch?</h3>
                        <h4>Januory 12, 2019</h4>
                    </span>
                </div>
                <hr>  
            </div>
            <!-- section 4  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-68.jpg" alt="blog-68">
                    <span>
                        <h3>The best augmented reality smartglasses</h3>
                        <h4>Januory 12, 2019</h4>
                    </span>
                </div>
                <hr>  
            </div>
            <!-- section 5  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-69.jpg" alt="blog-69">
                    <span>
                        <h3>12 Healthiest Foods to Eat for Breakfast</h3>
                        <h4>Januory 12, 2019</h4>
                    </span>
                </div> 
            </div>
        </div>
</template>

<script>
export default {
    name: 'PopularPost',
    data(){
        return{

        }
    }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
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
            color: $bg-grey-white ;
        }   
    }
}     
</style>

<template>
        <div class="section d-flex flex-column ">
            <h2>
                POPULAR POSTS
            </h2>
             <!-- section 1  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-55.jpg" alt="blog-55">
                    <span>
                        <h3>Simple Ways to Have a Pretty Face</h3>
                        <h4>January 12, 2019</h4>
                    </span>
                </div>
                <hr>  
            </div>
            <!-- section 2  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-56.jpg" alt="blog-56">
                    <span>
                        <h3>Ranking the greatest players in basketball</h3>
                        <h4>January 12, 2019</h4>
                    </span>
                </div>
                <hr>  
            </div>
            <!-- section 3  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-57.jpg" alt="blog-57">
                    <span>
                        <h3>4 Ways to Look Cool in Glasses</h3>
                        <h4>Januory 12, 2019</h4>
                    </span>
                </div>
                <hr>  
            </div>
            <!-- section 4  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-58.jpg" alt="blog-58">
                    <span>
                        <h3>Top Camper Trailer Towing Tips</h3>
                        <h4>Januory 12, 2019</h4>
                    </span>
                </div>
                <hr>  
            </div>
            <!-- section 5  -->
            <div class="popular d-flex flex-column">
                <div class="section-popular d-flex">
                    <img src="../../assets/img/blog-59.jpg" alt="blog-59">
                    <span>
                        <h3>5 Lovely Walks in New York</h3>
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
                cursor: pointer;
                &:hover{
                    transform: scale(200%);
                } 
            }
            span{
                
                h3{
                    color: $txt-black;
                    font-weight: 400;
                    margin-left: 10px;
                    cursor: pointer;
                    &:hover{
                        text-decoration: underline;
                    }
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

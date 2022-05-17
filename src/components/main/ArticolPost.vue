<template>
    <div class="container-fluid p-0 row">
        <div class="container-card p-0 col-9 debug">
          <!-- 1 artical  -->
            <div v-for="(detail, index) in dati" :key="index">
              <!-- <img :src="require(`${detail.img}`)" alt=""> -->
              <img src="../../assets/img/blog-54.jpg" alt="">
                <div class="articol debug2 d-flex">
                    <div class="date debug col-1">
                        <div class="day text-center">{{detail.date}}</div>
                        <div class="month text-center">JAN</div>
                    </div>
                    <div class="col-11 debug text">
                    {{detail.text}}
                        <div class="">
                            <span class="name">
                                {{detail.author}}
                            </span>
                            <span class="section">
                                {{detail.section}}
                            </span>
                            <span class="comments">
                                {{detail.comments}}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
            
        </div>


      <!-- social -->
        <div class="social debug2 col-3">
            <h2>LATEST FROM TWITTER</h2>
            <div class="twitter">
                <div>
                    <h4>If you have any suggestions for the next
                    updates, let us know.
                    </h4>
                    <a href="#">01:05 PM Sep 18th</a>
                </div>
                <div>
                    <h4>We have just updated Porto Admin. Check
                     the changelog for more information.
                    </h4>
                    <a href="#">01:05 PM Sep 18th</a>
                </div>
            </div>
            <!-- instagram  -->
            <div class="instagram-container">
                <h2>PHOTOS FROM INSTAGRAM</h2>
                <div class="instagram">
                    <div class="instagram-pictur">
                        <img src="../../assets/img/29739607_2020680068220520_4509928046932787200_n.jpg" alt="">
                    
                        <img src="../../assets/img/30087804_253872848488989_8792603541668626432_n.jpg" alt="">
                    
                        <img src="../../assets/img/29415620_196477127626244_3250318472361541632_n.jpg" alt="">
                   
                        <img src="../../assets/img/30078414_1274410412703843_8290935809419247616_n.jpg" alt="">
                    
                        <img src="../../assets/img/30077195_2066750973610181_3733150062893596672_n.jpg" alt="">
                    
                        <img src="../../assets/img/29415304_166583630713703_1032667922171953152_n.jpg" alt="">
                    </div>
                </div>
                <h2 class="tag">TAGS</h2>
                <div class="button ">
                    <span><a href="#">DESIGN</a></span>
                    <span><a href="#">BRANDS</a></span>
                    <span><a href="#">VIDEOS</a></span>
                    <span><a href="#">BUSINESS</a></span>
                    <span><a href="#">TRAVEL</a></span>
                </div>
            </div>
            <!-- find  -->
            <div class="find">
                <h3>FIND US ON FACEBOOK</h3>
                <div>
                    <a href="#">OKler Themes</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import LastPost from '../../LastPost'
export default {
    name: 'ArticolPost',
    data(){
        return{
            dati: LastPost,

        }
    }
}
</script>


<style lang="scss" scoped>
@import "../style/general.scss";
.container-fluid{
    width: 80%;
    margin: 40px auto;
    .container-card{
        min-height: 60vh;
        img{
            width: 100%;
        }
        .articol{
            width: 100%;
            .date{
                .day{
                    background-color: $bg-white-dark;
                    height: 60px;
                    width: 40px;
                    line-height: 60px;
                    font-weight: 700;
                }
                .month{
                    background-color: $bg-black;
                    color: $txt-white;
                    height: 20px;
                    width: 40px;
                    font-size: 0.7rem;
                    line-height: 20px;
                    font-weight: 700;
                }
            }
        }
    }
    .social{
        // position: fixed;
        // right: 0;
        // top: 0;
        h2{
            font-weight: 600;
        }
        .twitter{
            div{
                h4{
                    color: $txt-grey;
                }
            }
        }
        .instagram-container{
            margin-top: 30px;
            .instagram{
             
                .instagram-pictur{
                    
                    img{
                      width: 90px;
                      height: 90px;
                    }  
                }
                    
            }
            .tag{
                margin-top: 20px;
            }
            .button{
                margin-top: 20px;
                margin-bottom: 20px;
                span{
                    background-color: $bg-black;
                    padding-bottom: 3px;
                    padding-left: 3px;
                    padding-right: 3px;
                    border-radius: 10px;
                    margin-left: 2px;
                    
                    a{
                        font-size: 0.6rem;
                        color: $bg-white;
                        text-decoration: none;
                        font-weight: 700;
                        
                    }
                }
            }
        }
        .find{
            margin-top: 50px;
            div{
                border-left: 5px solid $br-white2;
                height: 40px;
                a{
                    text-decoration: none;
                    color: $txt-blue;
                    margin-left: 10px;
                    line-height: 40px;
                }
            }
        }
    }
    
}



</style>
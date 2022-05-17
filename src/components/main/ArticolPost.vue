<template>
    <div class="container-fluid p-0 row">
        <div class="container-card p-0 col-9 ">
          <!-- 1 artical  -->
            <div  v-for="(detail, index) in dati" :key="index">
              <!-- <img :src="require(`${detail.img}`)" alt=""> -->
              <img class="margin-top" :src="require('../../assets/img/' + detail.img)" alt="">
                <div class="articol margin-top d-flex">
                    <div class="date  col-1">
                        <div class="day text-center">{{detail.date}}</div>
                        <div class="month text-center">JAN</div>
                    </div>
                    <div class="col-11  text">
                        <h2>{{detail.title}}</h2>
                        <h3>{{detail.text}}</h3>
                        <div class="detail">
                            <span class="name">
                                <i class="fa-regular fa-user"></i>
                                <a href="#">{{detail.author}}</a>
                            </span>
                            <span class="section">
                                <i class="fa-regular fa-folder"></i>
                                <a href="#">{{detail.section}}</a>
                            </span>
                            <span class="comments">
                                <i class="fa-regular fa-comments"></i>
                                <a href="#">{{detail.comments}}</a>
                            </span>
                            <div class="float-end read-more">
                            
                                <a href="#">READ MORE</a>
                                
                        
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
        </div>


      <!-- social -->
        <div class="social  col-3">
            <h2>LATEST FROM TWITTER</h2>
            <div class="twitter">
               
                <div class="d-flex ">
                    <div>
                        <i class="fa-brands fa-twitter"></i>
                    </div>
                    <div>
                        <h4>If you have any    suggestions for the next
                        updates, let us know.
                        </h4>
                         <a href="#">01:05 PM Sep 18th</a> 
                    </div>
                    
                </div>
                <div class="d-flex">
                    <div>
                        <i class="fa-brands fa-twitter"></i>
                    </div>
                    <div>
                        <h4>We have just updated Porto Admin. Check
                         the changelog for more information.
                        </h4>
                        <a href="#">01:05 PM Sep 18th</a>
                    </div>
                    
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
@import "../style/variables.scss";
.container-fluid{
    width: 80%;
    margin: 0 auto;
    margin-bottom: 50px;
    .container-card{
        min-height: 60vh;
        img{
            width: 100%;
            margin-top: 40px;
        }
        .articol{
            width: 100%;
            .date{
                .day{
                    background-color: $bg-white-dark;
                    height: 50px;
                    width: 40px;
                    line-height: 50px;
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

            .text{
                
                h2{
                    font-size: 1.2rem;
                    font-weight: 600;
                }
                h3{
                    font-weight: 400;
                    color: $txt-grey;
                }
                .detail{
                    border-bottom: 1px solid $br-grey-dark;
                    padding-bottom: 20px;
                    i{
                        margin-right: 8px;
                    }
                    a{
                        margin-right: 8px;
                        text-decoration: none;
                        color: $txt-blue;
                        
                    }
                    .read-more{
                        border: 1px solid $br-grey;
                        border-radius: 5px;
                        height: 30px;
                        a{
                            padding-left: 10px;
                            color: $txt-grey;
                            font-weight: 300;
                        }
                    }
                }
            }
        }
    }
    .social{
        // position: fixed;
        // right: 0;
        // top: 0;
        margin-top: 40px;
        h2{
            font-weight: 600;
        }
        .twitter{
            .d-flex{
                margin-top: 20px;
                i{
                    margin-right: 10px;
                }
            
                div{
                    h4{
                        color: $txt-grey;
                    }
                    a{
                        color: $txt-blue;
                    }
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
                        color: $txt-white;
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
    .margin-top{
        margin-top: 20px;
    }
}



</style>
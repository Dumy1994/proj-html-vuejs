<template>
        <div class="section d-flex flex-column ">
            <h2>
                RECENT POSTS
            </h2>
             <!-- section 1  -->
            <div class="popular d-flex flex-column" v-for="(item,index) in dati" :key="index">
                <div class="section-popular d-flex">
                    <img :src="require('../../assets/img/' + item.img)" alt="blog-65">
                    <span>
                        <h3>{{item.title}}</h3>
                        <h4>{{item.date}}</h4>
                    </span>
                </div>
                <hr>  
            </div>
           
            
            
        </div>
</template>

<script>
import RecentPost from '../../RecentPost'
export default {
    name: 'PopularPost',
    data(){
        return{
            dati: RecentPost,
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
            position: relative;
            img{
                width: 50px;
                cursor: pointer;
                &:hover{
                    transform: scale(200%);
                    z-index:10;
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

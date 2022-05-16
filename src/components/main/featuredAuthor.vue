<template>
    <div class="section d-flex flex-column ">
        <h2>
            FEATURED POSTS
        </h2>
        <div class="featured">
            <img class="margin-top" src="../../assets/img/blog-66.jpg" alt="blog-66">
            <div class="title">
                <span class="name">
                    RECIPES
                </span>
                <div class="info">
                    Tips to Help You Quickly Prepare your
                    Lunch
                </div>
            </div> 
        </div>
        
        <h2 class="margin-top">
            FEATURED AUTHOR
        </h2>
        <div class=" margin-top d-flex">
            <div>
                <img class="img-profile" src="../../assets/img/avatar.jpg" alt="">
            </div> 
            <div>
                <h2 class="margin-left">John Doe</h2>
                <p class="margin-left">Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam quo assumenda placeat corrupti fugit esse commodi nulla ipsam culpa dolores?</p>
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
@import "../style/general.scss";
.section{
    width: 30%;
    .featured{
        position: relative;
        img{
            width: 100%;
        }
        .title{
            position: absolute;
            left: 10px;
            bottom: 10px;
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
    .img-profile{
        height: 100px;
    }
    
}   
.margin-top{
    margin-top: 30px;
}
.margin-left{
    margin-left: 10px;
}
p{
    color: $txt-grey-white;
}
</style>


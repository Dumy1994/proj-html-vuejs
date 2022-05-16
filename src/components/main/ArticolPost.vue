<template>
    <div class="container-fluid p-0 row">
        <div class="container-card p-0 col-9 debug">
          <!-- 1 artical  -->
            <div v-for="(detail, index) in dati" :key="index">
              <img src="../../assets/img/blog-54.jpg" alt="">
                <div class="articol debug2 d-flex">
                    <div class="date debug col-1">
                        <div>{{detail.date}}</div>
                        <div>JAN</div>
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
    margin: 0 auto;
    .container-card{
        min-height: 60vh;
        img{
            width: 100%;
        }
        .articol{
            width: 100%;
        }
    }
    .social{
        
        min-height: 50vh;
    }
}



</style>
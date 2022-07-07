<template>
        <div class="section d-flex flex-column ">
            
            <h2>
                RECENT POSTS
            </h2>
            
             <!-- section 1  -->
            <div class="popular d-flex flex-column" v-for="(item,index) in textShow" :key="index">
                <div class="section-popular d-flex">
                    <img :src="require('../../assets/img/' + item.img)" alt="blog-65">
                    <span>
                        <h3>{{item.title}}</h3>
                        <h4>{{item.date}}</h4>
                    </span>
                </div>
                <hr>  
            </div>
            <search-post @mySearch="setTextSearch($event) "/>
           
            
            
        </div>
</template>

<script>
import RecentPost from '../../RecentPost'
import SearchPost from './SearchPost.vue'
export default {
  components: { SearchPost },
    name: 'PopularPost',
    data(){
        return{
            dati: RecentPost,
            searchText:'',
            
            
        }
    },
    methods:{
       setTextSearch(text){
           this.searchText = text
       },
       empity(){
            if(this.inputText == ''){
          return this.notFound = true
        }else{
          return this.notFound = false
        }
       }
       
    },
    computed:{
        textShow(){
            return this.dati.filter((el)=>el.title.toLowerCase().includes(this.searchText.toLowerCase()));
           
            
            
        }
        // listSearch(){
        //   return this.textShow = this.dati.filter((el)=>{
        //      if(el.title.toLowerCase().includes(this.searchText.toLowerCase())){
        //          return true
        //      }else{
        //          return false
        //      }
        //     })
        //     return this.textShow,
        //     console.log(this.textShow)

        // },
    },
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

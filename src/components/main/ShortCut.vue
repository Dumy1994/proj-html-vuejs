<template>
  <section class="container-fluid p-0 short">
      <ul class="d-flex justify-content-between p-0 align-items-center">
          <li @click="prevSlide"><i class="fa-solid text-center  fa-angle-left"></i></li>
          <li  v-for="(item, index) in short.slice(n, nMax)" :key="index">
              <a  href="#" >{{item}}</a>
          </li>
          <li @click="nextSlide"><i  class="fa-solid text-center fa-angle-right"></i></li>
      </ul>

  </section>
</template>

<script>
export default {
    name: 'ShortCut',
    data(){
        return{
            short:['GADGETS','PHOTOGRAPHY', 'LIFESTYLE', 'FASHION', 'RECIPES', 'TRAVEL','ARCHITECTURE','REVIEWS','SPORTS','VIDEOS','TECHNOLOGY','DESIGN'],
            nMax: 5,
            n: 0,
            

        }
    },
    methods:{
        
        nextSlide(){
            this.nMax = this.nMax +1
            if(this.nMax >= 12){
                this.nMax = 12
            }
    
            this.n = this.n +1
             
            if(this.n >= 7){
                this.n = 7
            }
            console.log(this.nMax)
            console.log(this.n)
        },
        prevSlide(){
            this.nMax = (this.nMax <= 5) ? 5 :this.nMax -= 1;
            this.n = this.n -=1
            if(this.n <=0){
                this.n = 0
            }
            
          
        },
    },
    
}

</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.short{
    height: 10vh;
    margin-top: 30px;
    background-color: $bg-blue;
    ul{
        width: 80%;
        margin: 0 auto;
        list-style: none;
        li{
            line-height: 10vh;
            
            a{
                text-decoration: none;
                height: 20px;
                background-color: $bg-grey-dark2;
                color: $txt-white;
                padding: 10px;
                width: 60px;
                &:hover{
                    background-color: $bg-black2;
                }
            }
            i{
                color: $bg-grey-dark2;
                cursor: pointer;
                border: 2px solid $bg-grey-dark2;
                padding: 5px;
                height: 30px;
                width: 30px;
                border-radius: 50%;
                &:hover{
                    transform: scale(130%);
                    
                }
            }
        }
    }
}
</style>
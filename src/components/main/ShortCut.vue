<template>
  <section class="container-fluid p-0 short">
      <ul class="d-flex justify-content-between p-0 align-items-center">
          <li @click="prevSlide"><i class="fa-solid text-center  fa-angle-left"></i></li>
          <li  v-for="(item, activeIndex) in short.slice(n, activeIndex)" :key="activeIndex">
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
            activeIndex: 5,
            n: 0,
            

        }
    },
    methods:{
        
        nextSlide(){
            this.activeIndex = (this.activeIndex === 13) ? 5 : this.activeIndex += 1;
            this.n = (this.n <= 5) ? this.n +1 : this.n -= 1; 
            console.log(this.activeIndex)
            console.log(this.n)
        },
        prevSlide(){
            this.activeIndex = (this.activeIndex <= 5) ? 5 :this.activeIndex -= 1;
            this.n = (this.n >= 0) ? this.n -=1 : this.n += 1
            console.log(this.activeIndex)
            console.log(this.n)
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
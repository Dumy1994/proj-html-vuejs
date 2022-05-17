<template>
  <section class="container-fluid p-0 short">
      <ul class="d-flex justify-content-between p-0 align-items-center">
          <li @click="prevSlide"><i class="fa-solid fa-angle-left"></i></li>
          <li  v-for="(name, activeIndex) in short.slice()" :key="activeIndex">
              <a  href="#" >{{name}}</a>
          </li>
          <li @click="nextSlide"><i  class="fa-solid fa-angle-right"></i></li>
      </ul>

  </section>
</template>

<script>
export default {
    name: 'ShortCut',
    data(){
        return{
            short:['GADGETS','PHOTOGRAPHY', 'LIFESTYLE', 'FASHION', 'RECIPES', 'TRAVEL','ARCHITECTURE','REVIEWS','SPORTS','VIDEOS','TECHNOLOGY','DESIGN'],
            activeIndex: 0,

        }
    },
    methods:{
        nextSlide(){
            this.activeIndex = (this.activeIndex === 8) ? 0 : this.activeIndex += 1;
            console.log(this.activeIndex)
        },
        prevSlide(){
            this.activeIndex = (this.activeIndex === 0) ? 8 : this.activeIndex -= 1;
            console.log(this.activeIndex)
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
            }
        }
    }
}
</style>
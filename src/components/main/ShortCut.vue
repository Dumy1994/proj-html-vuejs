<template>
  <section class="container-fluid p-0 short">
      <ul class="d-flex justify-content-around align-items-center">
          <li  v-for="(name, index) in short" :key="index">
              <a  href="#">{{name}}</a>
          </li>
      </ul>

  </section>
</template>

<script>
export default {
    name: 'ShortCut',
    data(){
        return{
            short:['GADGETS','PHOTOGRAPHY', 'LIFESTYLE', 'FASHION', 'RECIPES', 'TRAVEL']
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.short{
    height: 15vh;
    margin-top: 10px;
    background-color: $bg-blue;
    ul{
        list-style: none;
        li{
            line-height: 15vh;
            a{
                text-decoration: none;
                height: 20px;
                background-color: $txt-black2;
                color: $txt-white;
                padding: 10px;
                width: 60px;
            }
        }
    }
}
</style>
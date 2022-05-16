<template>
  <section class="container-fluid p-0 debug">
    <div class=" container-section d-flex justify-content-between">
        <popular-post/>

    </div>

  </section>
</template>

<script>
import PopularPost from './PopularPost.vue'
export default {
  components: { PopularPost },
    name: 'AppPost',
    data(){
        return{

        }
    }
}
</script>

<style lang="scss" scoped>
@import "../style/general.scss";
    section{
        min-height: 50vh;
        .container-section{
             width: 80%;
            margin: 20px auto;
        }
       
        
    }
</style>

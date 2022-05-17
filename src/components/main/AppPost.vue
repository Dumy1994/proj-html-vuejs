<template>
  <section class="container-fluid p-0 ">
    <div class=" container-section d-flex justify-content-between">
        <popular-post/>
        <recent-post/>
        <featured-author/>
    </div>

  </section>
</template>

<script>
import FeaturedAuthor from './featuredAuthor.vue'
import PopularPost from './PopularPost.vue'
import RecentPost from './RecentPost.vue'
export default {
  components: { PopularPost, RecentPost, FeaturedAuthor },
    name: 'AppPost',
    data(){
        return{

        }
    }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
    section{
        min-height: 50vh;
        .container-section{
             width: 80%;
            margin: 20px auto;
        }
       
        
    }
</style>

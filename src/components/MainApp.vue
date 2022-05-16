<template>
  <div>
   <feautured-post/>
   <app-post/>
   <short-cut/>
   <articol-post/>
   
  </div>
</template>

<script>
import AppPost from './main/AppPost.vue'
import ArticolPost from './main/ArticolPost.vue'
import FeauturedPost from './main/FeauturedPost.vue'
import ShortCut from './main/ShortCut.vue'


export default {
  components: {FeauturedPost, AppPost, ShortCut, ArticolPost},
 
     name:'MainApp',
  data(){
        return{
            
        }
    },
    methods:{
       
       
    },
    computed:{

    },
}
</script>

<style lang="scss">

</style>
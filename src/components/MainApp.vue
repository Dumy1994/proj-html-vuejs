<template>
  <div>
   <feautured-post/>
   <app-post/>
   <short-cut/>
   
  </div>
</template>

<script>
import AppPost from './main/AppPost.vue'
import FeauturedPost from './main/FeauturedPost.vue'
import ShortCut from './main/ShortCut.vue'


export default {
  components: {FeauturedPost, AppPost, ShortCut},
 
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
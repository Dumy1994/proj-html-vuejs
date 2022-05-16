<template>
  <div>
   <feautured-post/>
   <app-post/>
   
  </div>
</template>

<script>
import AppPost from './main/AppPost.vue'
import FeauturedPost from './main/FeauturedPost.vue'


export default {
  components: {FeauturedPost, AppPost},
 
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
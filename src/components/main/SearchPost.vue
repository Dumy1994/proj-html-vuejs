<template>
            
  <div class="input-search">
        <input type="text" placeholder="Type and hit enter ..."   v-model="inputText" @keyup.enter="search">
        <!-- <h2 v-show="notFound == true">NOT FOUND ANY</h2> -->
  </div>
</template>

<script>
export default {
    name:'SearchPost',
    data(){
      return{
        inputText: '',
        notFound: false
      }
    },
    methods:{
      search(){
        this.$emit('mySearch', this.inputText)
        this.inputText = '';
        // if(this.inputText == ''){
        //   return this.notFound = true
        // }else{
        //   return this.notFound = false
        // }
      }
    },
}
</script>

<style lang="scss">
@import "../style/variables.scss";

.input-search{
        input{
          width: 100%;
          background-color: $bg-trasparent;
          color: $txt-blue;
          border-top: none;
          border-right: none;
          border-left: 2px solid $txt-blue;
          border-bottom: 2px solid $txt-blue;
        }

      }


::placeholder {
  color: $txt-blue;
  padding: 10px;
  }

</style>
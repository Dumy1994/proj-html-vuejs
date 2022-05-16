<template>
  <div id="app">
    <!-- header  -->
    <header>
      <header-app/>
    </header>
    <!-- main  -->
    <main>
      <main-app/>
    </main>
    <!-- footer  -->
    <footer>
      <footer-app/>
    </footer>

  </div>
</template>

<script>
import FooterApp from './components/FooterApp.vue'
import HeaderApp from './components/HeaderApp.vue'
import MainApp from './components/MainApp.vue'


export default {
  name: 'App',
  components: {
    HeaderApp,
    MainApp,
    FooterApp
    
  },
  data(){
    return{

    }
  }
}
</script>

<style lang="scss">
@import "./components/style/general.scss";

</style>

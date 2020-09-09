<template>
  <div id="app">
   <link rel="stylesheet" href="node_modules/@fortawesome/fontawesome-free/css/all.css">
    <Header/>
    <div class="main-content">
      <router-view/>  
    </div>
    <Welcome/>
    <Vision/>
    <Careers/>
    <Footer/>
    
  </div>
</template>


<script>
  import Header from '@/components/header/Header.vue'
  import Welcome from '@/components/Welcome.vue'
  import Vision from '@/components/Vision.vue'
  import Careers from '@/components/Careers.vue'
  import Footer from '@/components/footer/Footer.vue'
 export default {
  name: 'App',
  components: {
    Header,
    Welcome,
    Vision,
    Careers,
    Footer
  }
} 
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}



</style>

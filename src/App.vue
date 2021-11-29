<template>
  <div class ="container">
    <Navbar/>
  <router-view class="espacio-contenido"/>
    <Footer/>
</div>
</template>
<script>
import Navbar from "./components/Navbar.vue"
import Footer from "./components/Footer.vue"
export default {
  components : { 
    Navbar, Footer
  }
}
  
</script>
<style>
.espacio-contenido{
  padding-bottom : 20px;
  padding-top : 20px
}
</style>

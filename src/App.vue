<template>
  <div id="app">
    <Header />
    <router-view/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/header';
import Footer from './components/footer'; 
export default {
  name:"app",
  components: {
    Header,
    Footer
  }
}
</script>

<style>
  #app {
  text-align: center;
}
</style>


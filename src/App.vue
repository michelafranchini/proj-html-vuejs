<template>
  <div id="app">
    <Header />

    <Main :tag="tags"/>
    
    <Footer :categories="tags"/>
  </div>
</template>

<script> 
import Header from './components/Header.vue'; 
import Main from './components/Main.vue'; 
import Footer from './components/Footer.vue'; 


export default {
  name: 'App',
  components: {
    Header, 
    Main, 
    Footer,
  }, 
  data() {
    return {
      tags: [
        {
          link: "", 
          tag: "gadgets"
        }, 
        {
          link: "", 
          tag: "photography"
        },
        {
          link: "", 
          tag: "lifestyle"
        },
        {
          link: "", 
          tag: "fashion"
        },
        {
          link: "", 
          tag: "recipes"
        },
        {
          link: "", 
          tag: "travel"
        },
        {
          link: "", 
          tag: "business"
        },
        {
          link: "", 
          tag: "architecture"
        },
        {
          link: "", 
          tag: "reviews"
        },
        {
          link: "", 
          tag: "sports"
        },
        {
          link: "", 
          tag: "videos"
        },
        {
          link: "", 
          tag: "technology"
        },
        {
          link: "", 
          tag: "design"
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import './style/variables.scss';
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import "~@fontsource/montserrat/400.css";
// @import '~bootstrap/scss/bootstrap.scss' ; 

  body {
    font-family: 'Montserrat', sans-serif;
    box-sizing: border-box;
    margin: 0;
    padding: 0;

  }

</style>

<template>
  <header>
        <div class="bg_blue">
            <div class="container_75">
                <div class="top_header">
                    <p>Evertything about Lifestyle, Travel and Gadgets!</p>
                    <ul>
                        <li>sign in</li>
                        <li>about us</li>
                        <li>contact us</li>
                        <li>buy now</li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="logo_container">
            <div class="container_75">
                <img src="../assets/images/logo-default-slim.png" alt="">
            </div>
        </div>
        <div class="container_75">
            <Navbar :item="navbar"/>
        </div>
        <div>
            <Jumbotron :jumbotronArticle="jumbotronList"/>
        </div>

  </header>
</template>

<script>
import Navbar from '../components/Navbar.vue'; 
import Jumbotron from '../components/Jumbotron.vue'; 

export default {
    name: "Header", 
    components: {
        Navbar, 
        Jumbotron
    }, 
    data() {
        return {
            navbar: [
                {
                    name: "home", 
                    link: ""
                }, 
                {
                    name: "elements", 
                    link: ""
                }, 
                {
                    name: "features", 
                    link: ""
                }, 
                {
                    name: "pages", 
                    link: ""
                }, 
                {
                    name: "portfolio", 
                    link: ""
                }, 
                {
                    name: "blog", 
                    link: ""
                }, 
                {
                    name: "shop", 
                    link: ""
                }

            ], 
            jumbotronList : [
                {
                    title: "how to take better concert pictures in 30 seconds", 
                    link: require("../assets/images/blog-46.jpg"), 
                    tag: "photography", 
                },
                {
                    title: "gadgets taht make your smartphone even smarter", 
                    link: require("../assets/images/blog-47.jpg"), 
                    tag: "gadgets", 
                },
                {
                    title: "20 top-rated tourist attractions in manhattan", 
                    link: require("../assets/images/blog-48.jpg"), 
                    tag: "travel", 
                },
                {
                    title: "the best way to ride a motorcycle", 
                    link: require("../assets/images/blog-49.jpg"), 
                    tag: "lifestyle", 
                },
                {
                    title: "5 fun things to do al the beach", 
                    link: require("../assets/images/blog-50.jpg"), 
                    tag: "travel", 
                },
                {
                    title: "amazingly fresh fruit and herb drinks for summer", 
                    link: require("../assets/images/blog-51.jpg"), 
                    tag: "recipes", 
                }, 
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
// @import '~bootstrap/scss/bootstrap.scss' ;  
@import './src/style/variables.scss'; 


    .bg_blue {
        height: 50px;
        color: white;
        background-color: #0088cc;
    }

    .container_75 {
        width: 75%;
        margin: auto;

        p {
            font-size: 13px;
            color: #c0e2f2;
        }

    }
    .top_header {
        display: flex;
        align-items: center;
        height: 50px;

        ul {
            margin: 0 30px;
            padding: 0;

            li {
            display: inline-block;
            list-style: none;
            text-transform: uppercase;
            cursor: pointer;
            padding: 15px;
            font-size: 12px;
            color: white;
        }

    }

    }
    .logo_container {
        display: flex;
        align-items: center;
        height: 130px; 
        border-bottom: 1px solid #ededed;
        
        img {
            width: 100px;
        }
    }
    
</style>
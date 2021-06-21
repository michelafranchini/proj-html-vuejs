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
  </header>
</template>

<script>
import Navbar from '../components/Navbar.vue'

export default {
    name: "Header", 
    components: {
        Navbar
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
            margin-bottom: 0;
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


        // &:hover {
        //     color: #0088cc;
        // }

        // &:active {
        //     color: #0088cc;
        // }

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
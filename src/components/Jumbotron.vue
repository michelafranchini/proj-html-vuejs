<template>
    <div class="bg_grey">
        <div class="container_75">
            <div v-for="article, index in jumbotronArticle" :key="index" class="single_article">
                <div class="text_article_jmb">
                    <h4>{{article.tag}}</h4>
                    <h2>{{article.title}}</h2>
                    <p>{{article.text}}</p>
                </div>
                <img :src="article.link" :alt="article.title" class="jmbimg">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Jumbotron", 
    props: ["jumbotronArticle"], 

    data() {
        return {
            // path: "../assets/images/",
        }
    }
}
</script>

<style lang="scss" scoped>
    .bg_grey {
        background-color: #f7f7f7;
        padding: 30px 0;
    }

    .container_75 {
        width: 75%;
        margin: auto;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }

    h4 {
        display: inline-block;
        text-transform: uppercase; 
        font-size: 12px;
        padding: 5px;
        border-radius: 3px;
        background-color: #0088cc;
        color: white;
    }

    h2 {
        text-transform: capitalize;
        font-size: 20px; 
        font-weight: bold;
        margin: 0;
        color: white;
    }

    p {
        display: none;
        font-weight: bold;
        font-size: 13px;
        color: #b7b7b7;
    }

    .text_article_jmb {
        position: absolute;
        bottom: 0;
        left: 0;
        padding: 30px;
        z-index: 2;
    }


    .jmbimg {
        height: 100%;
        width: 100%;
    }

    .single_article {
        width: 32%; 
        height: 270px;
        margin-bottom: 30px;
        position: relative;
        cursor: pointer;
        

        &::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.4);

        }

        &:hover p {
            display: block;
        }
        
    }
</style>
<template>
  <section>
    <div v-for="post, index in post" :key="index" class="post_container">
        <img :src="post.url" alt="">
        <div>
            <h4>{{post.title}}</h4>
            <p>{{post.date}}</p>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "Post", 
    props: ["post"]
}
</script>

<style lang="scss" scoped>
    * {
        box-sizing: border-box;
        padding: 0;
        margin: 0;
    }
    img {
        width: 50px;
        height: 50px;
        margin-right: 10px;
    }
    h4 {
        font-size: 13px;
        color: #212529;
    }
    p {
        font-size: 10px;
        color: #888888 ;
    }

    h4, p {
        text-transform: capitalize;
        padding: 5px;
    }

    section {
        margin-right: 20px;
    }
    .post_container {
        display: flex;
        margin: 10px 0;
        padding: 10px 0;
        border-bottom: 1px dotted #E2E2E2;

        
    }
</style>
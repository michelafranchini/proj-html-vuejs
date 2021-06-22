<template>
  <main>
    <div class="container_75 first_section">
      <div class="post_section">
        <h3>popular posts</h3>
        <Post :post="popularPosts"/>
      </div>
      <div class="post_section">
        <h3>recent posts</h3>
        <Post :post="recentPosts" />
      </div>
      <div class="post_section">
        <h3>featured posts</h3>
      </div>
    </div>

    <Slider :sliderTags="tag"/>

    <div class="container_75">
      <Card :card="card"
      v-for="card, index in cards" 
      :key="index"
      />
    </div>
  </main>
</template>

<script>
import Post from '../components/Post.vue'; 
import Slider from '../components/Slider.vue'; 
import Card from '../components/Card.vue'

export default {
    name: "Main", 
    components: {
      Post, 
      Slider, 
      Card
    }, 
    props: ["tag"], 
    data() {
      return {
        popularPosts: [
          {
            url: require("../assets/images/blog-55.jpg"), 
            title: "simple ways to have a pretty face", 
            date: "January 12, 2019"
          }, 
          {
            url: require("../assets/images/blog-56.jpg"), 
            title: "ranking the greatest players in basketball", 
            date: "January 12, 2019"
          }, 
          {
            url: require("../assets/images/blog-57.jpg"), 
            title: "4 ways to look cool in glasses", 
            date: "January 12, 2019"
          },
          {
            url: require("../assets/images/blog-58.jpg"), 
            title: "top camper trailer towing tips", 
            date: "January 12, 2019"
          },
          {
            url: require("../assets/images/blog-59.jpg"), 
            title: "5 lovely walks in new york", 
            date: "January 12, 2019"
          }, 
        ], 
        recentPosts: [
          {
            url: require("../assets/images/blog-65.jpg"), 
            title: "main reasons to stop texting and driving", 
            date: "January 12, 2019"
          }, 
          {
            url: require("../assets/images/blog-66.jpg"), 
            title: "tips to help you qickly prepare your lunch", 
            date: "January 12, 2019"
          }, 
          {
            url: require("../assets/images/blog-67.jpg"), 
            title: "why should i buy a smartwatch?", 
            date: "January 12, 2019"
          },
          {
            url: require("../assets/images/blog-68.jpg"), 
            title: "the best augmented reality smartglasses", 
            date: "January 12, 2019"
          },
          {
            url: require("../assets/images/blog-69.jpg"), 
            title: "12 healtiest food to eat for breakfast ", 
            date: "January 12, 2019"
          }, 
        ], 
        cards: [
          {
            url: require("../assets/images/blog-54.jpg"), 
            title: "how to make friends as a grown-up",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit, aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos, qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui dolorem ipsum.",
            author: "John Doe", 
            tags: "Lifestyle, Travel", 
            comments: "12 Comments", 
            date: "January 12, 2019"
          },
          {
            url: require("../assets/images/blog-55 (1).jpg"), 
            title: "Simple ways to have a pretty face",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit, aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos, qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui dolorem ipsum.",
            author: "John Doe", 
            tags: "Photography, Travel", 
            comments: "12 Comments", 
            date: "January 12, 2019"
          },
          {
            url: require("../assets/images/blog-56 (1).jpg"), 
            title: "ranking the greatest players in basketball",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit, aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos, qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui dolorem ipsum.",
            author: "John Doe", 
            tags: "Sport, Business", 
            comments: "12 Comments", 
            date: "January 12, 2019"
          },
          {
            url: require("../assets/images/blog-58 (1).jpg"), 
            title: "top camper trailer towing tips",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit, aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos, qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui dolorem ipsum.",
            author: "John Doe", 
            tags: "Travel, Lifestyle", 
            comments: "12 Comments", 
            date: "January 12, 2019"
          },
          // {
          //   url: [ 
          //     require("../assets/images/blog-13.jpg"), 
          //     require("../assets/images/blog-16.jpg"), 
          //     require("../assets/images/blog-20.jpg"), 
          //     require("../assets/images/blog-23.jpg"),
          //     require("../assets/images/blog-29.jpg"), 
          //     require("../assets/images/blog-40.jpg")
          //   ], 
          //   title: "10 best travel tips after 5 years traveling the world",
          //   text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit, aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos, qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui dolorem ipsum.",
          //   author: "John Doe", 
          //   tags: "Travel, Lifestyle", 
          //   comments: "12 Comments", 
          //   date: "January 12, 2019"
          // },
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
  .container_75 {
    width: 75%;
    margin: auto;

    .post_section {
      width: 30%;
    }
    h3 {
      color: black;
    }
    
  }

  .first_section {
    display: flex;
  }
</style>
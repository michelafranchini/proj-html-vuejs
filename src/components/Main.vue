<template>
  <main>
    <div class="container_75 first_section">
      <!-- sezione con la lista dei post recent e popular -->
      <div class="post_section">
        <h3>popular posts</h3>
        <Post :post="popularPosts"/>
      </div>
      <div class="post_section">
        <h3>recent posts</h3>
        <Post :post="recentPosts" />
      </div>
      <!-- /sezione con la lista dei post recent e popular -->

    <!-- articolo statico sulla destra dellla prima sezione del main -->
      <div class="post_section">
        <h3>featured posts</h3>
        <div class="right_article">
          <div class="text_article">
            <h4>recipes</h4>
            <h2>Tips to Help You Quickly Prepare Your Lunch</h2>
          </div>
          <img src="../assets/images/blog-66.jpg" alt="" class="jmbimg">
        </div>
        
        <h3>featured author</h3>
        <div class="author">
          <img src="../assets/images/avatar.jpg" alt="" class="avatar">
          <div>
            <h5>John Doe</h5>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste, sapiente.</p>
          </div>
        </div>
      </div>
      <!-- /articolo statico sulla destra dellla prima sezione del main -->
    </div>

    <Slider :sliderTags="tag"/>

    <!-- sezione con i vari articoli dle blog -->
    <div class="container_75 second_section">
      <div>
        <Card :card="card"
        v-for="card, index in cards" 
        :key="index"
        />

      </div>
      <!-- contatore pagine -->
      <div class="counter_page">
          <div class="page">
            <i class="fas fa-chevron-left"></i>
          </div>
          <div class="page">
            <p>1</p>
          </div>
          <div class="page">
            <p>2</p>
          </div>
          <div class="page">
            <p>3</p>
          </div>
          <div class="page">
            <i class="fas fa-chevron-right"></i>
          </div>
      </div>
      <!-- /contatore pagine -->

      <div>
        <TwitterAside />
      </div>
    </div>
    <!-- /sezione con i vari articoli dle blog -->
  </main>
</template>

<script>
import Post from '../components/Post.vue'; 
import Slider from '../components/Slider.vue'; 
import Card from '../components/Card.vue'; 
import TwitterAside from '../components/TwitterAside.vue'

export default {
    name: "Main", 
    components: {
      Post, 
      Slider, 
      Card, 
      TwitterAside
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
            date: "January 12, 2019", 
            calDay: "12", 
            calMonth: "JAN"
          },
          {
            url: require("../assets/images/blog-55 (1).jpg"), 
            title: "Simple ways to have a pretty face",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit, aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos, qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui dolorem ipsum.",
            author: "John Doe", 
            tags: "Photography, Travel", 
            comments: "12 Comments", 
            date: "January 12, 2019", 
            calDay: "12", 
            calMonth: "JAN"
          },
          {
            url: require("../assets/images/blog-56 (1).jpg"), 
            title: "ranking the greatest players in basketball",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit, aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos, qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui dolorem ipsum.",
            author: "John Doe", 
            tags: "Sport, Business", 
            comments: "12 Comments", 
            date: "January 12, 2019", 
            calDay: "12", 
            calMonth: "JAN"
          },
          {
            url: require("../assets/images/blog-58 (1).jpg"), 
            title: "top camper trailer towing tips",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit, aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos, qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui dolorem ipsum.",
            author: "John Doe", 
            tags: "Travel, Lifestyle", 
            comments: "12 Comments", 
            date: "January 12, 2019", 
            calDay: "12", 
            calMonth: "JAN"
          },
          {
            url: require("../assets/images/blogmix.png"), 
            title: "10 best travel tips after 5 years traveling the world",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit, aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos, qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui dolorem ipsum.",
            author: "John Doe", 
            tags: "Travel, Lifestyle", 
            comments: "12 Comments", 
            date: "January 8, 2019", 
            calDay: "8", 
            calMonth: "JAN"
          },
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
        font-size: 17px; 
        font-weight: bold;
        margin: 0;
        color: white;
    }
    .jmbimg {
        width: 100%;
    }
    }
    h3 {
      text-transform: uppercase;
      font-size: 15px;
      color: black;
    }
    
  }

  .first_section {
    display: flex;
    justify-content: space-between;
    margin-top: 50px; 
    margin-bottom: 50px;
  }
  .right_article {
    position: relative;

      &::after {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 98%;
        background-color: rgba(0, 0, 0, 0.4);

        }
  }
  .text_article {
    position: absolute;
    bottom: 10px;
    padding: 10px;
    z-index: 2;
  }

  .author {
    display: flex;
    .avatar {
      width: 130px;
      margin-right: 30px;
    }
    h5 {
      margin: 5px 0 10px 0;
      font-size: 17px;
    }
    p {
      line-height: 20px;
      font-size: 13px;
      color: #888888;
    }
    
  }

  .second_section {
    display: flex; 
    position: relative;
    margin-top: 50px; 
    margin-bottom: 50px; 
  }

  .counter_page {
    display: flex;
    width: 150px;
    height: 30px;
    position: absolute;
    bottom: 0;
    right: 0;
    transform: translate(-252%, 39%);
    color: #0088cc;

    .page {
      display: flex;
      justify-content: center;
      align-items: center; 
      cursor: pointer;
      width: 30px; 
      border: 1px solid #f0f0f0;

      &:hover {
        color: white;
        background-color: #0088cc;
      }

      p {
        margin: 0; 
      }
    }
  }

  
</style>
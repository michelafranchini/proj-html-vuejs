<template>
    <footer>
        <div class="bg_dark">
            <div class="container_75">
                <div class="about">
                    <h3>about the blog</h3>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Facere beatae error hic sit voluptate explicabo doloribus. Nulla hic impedit esse.</p>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Expedita a omnis similique quisquam ipsam odit maiores repellat corporis error molestias.</p>
                    <a href="#">view more<i class="fas fa-chevron-right"></i></a>
                </div>
                <div class="post">
                    <h3>recent posts</h3>
                    <div>
                        <img src="../assets/images/our-office-4-square.jpg" alt="">
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum, rem?</p>
                    </div>
                    <div>
                        <img src="../assets/images/our-office-5-square.jpg" alt="">
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum, rem?</p>
                    </div>
                </div>
                <div class="comments">
                    <h3>recent comments</h3>
                    <div>
                        <p>Lorem ipsum dolor sit amet.</p>
                    </div>
                </div>
                <div class="tags">
                    <h3>categories</h3>
                </div>
            </div>
        </div>
        <div class="bottom_footer">
            <div class="container_75">
                <img src="../assets/images/logo-footer.png" alt="logo footer">
                
            </div>

        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style lang="scss">
    .bg_dark {
        height: 300px;
        background-color: #212529;

        .container_75 {
            width: 75%;
            margin: auto;
            display: flex;
        }
    }

    .post {
        img {
            width: 80px;
            border-radius: 50%;
        }
    }

    h3 {
        text-transform: uppercase;
        font-size: 15px;
        color: white;
    }

    p {
        font-size: 13px;
        color: #777777;
    }

    .about {
        width: 30%;
        margin-right: 50px;

        a {
            text-decoration: none;
            text-transform: uppercase;
            font-size: 13px;
            color: white;

            i {
                font-size: 10px;
                margin-left: 5px;
            }

            &:hover {
                color: #0088CC;
            }
        }
    }

    .bottom_footer {
        background-color: #1c2023;
    }
</style>
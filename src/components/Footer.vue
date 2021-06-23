<template>
    <footer>
        <div class="bg_dark">
            <!-- label blu sopra footer -->
            <div class="label">
                <h2>get in touch</h2>
            </div>
            <!-- /label blu sopra footer -->

            <!-- footer in alto -->
            <div class="container_75 top_footer">
                <!-- colonna about -->
                <div class="about">
                    <h3>about the blog</h3>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Facere beatae error hic sit voluptate explicabo doloribus. Nulla hic impedit esse.</p>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Expedita a omnis similique quisquam ipsam odit maiores repellat corporis error molestias.</p>
                    <a href="#">view more<i class="fas fa-chevron-right"></i></a>
                </div>

                <!-- colonna post -->
                <div class="post">
                    <h3>recent posts</h3>
                    <div class="single_post">
                        <img src="../assets/images/our-office-4-square.jpg" alt="">
                        <div class="text_post">
                            <h5>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum, rem?</h5>
                            <p>12:53 AM Dec 19th</p>
                        </div>
                    </div>

                    <div class="single_post">
                        <img src="../assets/images/our-office-5-square.jpg" alt="">
                        <div class="text_post">
                            <h5>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum, rem?</h5>
                            <p>12:53 AM Dec 19th</p>
                        </div>
                    </div>
                </div>

                <!-- colonna con commenti e foto -->
                <div class="comments">
                    <h3>recent comments</h3>
                    <div class="comment">
                        <i class="fas fa-chevron-right"></i>
                        <div>
                            <p><span class="author">John Doe</span> commented on <span class="blue_span">lorem ipsum dolor sit amet.</span></p>
                            <p>12:53 AM Dec 19th</p>
                        </div>
                    </div>
                    <div class="comment">
                        <i class="fas fa-chevron-right"></i>
                        <div>
                            <p><span class="author">John Doe</span> commented on <span class="blue_span">lorem ipsum dolor sit amet.</span></p>
                            <p>12:53 AM Dec 19th</p>
                        </div>
                    </div>
                </div>

                <!-- colonna con i tag delle categorie -->
                <div class="tags">
                    <h3>categories</h3>
                    <ul>
                        <li v-for="categorie, index in categories"
                        :key="index">
                            {{categorie.tag}}
                        </li>
                    </ul>
                </div>
            </div>
            <!-- /footer in alto -->
        </div>

        <!-- bottom footer con logo -->
        <div class="bottom_footer">
            <div class="container_75">
                <div class="bottom_footer_left">
                    <img src="../assets/images/logo-footer.png" alt="logo footer">
                    <p>&#169; Copyright 2020. All Rights Reserved</p>
                </div>
                <div>
                    <ul>
                        <li><i class="fas fa-chevron-right"></i>FAQ's</li>
                        <li><i class="fas fa-chevron-right"></i>Sitemap</li>
                        <li><i class="fas fa-chevron-right"></i>Contact Us</li>
                    </ul>
                </div>
            </div>

        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer", 
    props: ["categories"]
}
</script>

<style lang="scss" scoped>
@import "~@fontsource/shadows-into-light/400.css";
    * {
        margin: 0;
        padding: 0;
    }

    h3 {
        text-transform: uppercase;
        margin-bottom: 20px;
        font-size: 15px;
        color: white;
    }

    p {
        font-size: 13px;
        color: #777777;
    }

    h5 {
        color: #B7B7B7;
    }

    .container_75 {
        width: 75%;
        margin: auto;
    }
    // top footer

    .bg_dark {
        position: relative;
        height: 400px;
        background-color: #212529;
    }

    .top_footer {
        height: 400px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .about {
        width: 25%;
        margin-right: 50px;

        p {
            margin: 0 0 15px 0;
            line-height: 25px;
        }

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

    .post {
        width: 25%;
        .single_post {
            display: flex;
            align-items: center;

            img {
                width: 80px;
                margin: 0px 15px 15px 0;
                border-radius: 50%;
            }
        }
    }

    .comments {
        width: 25%;
        .comment {
            display: flex;
            align-items: baseline;
            margin-bottom: 15px;
            p {
                margin: 0 0 15px 0; 
            }
            i {
                margin-right: 5px;
                font-size: 10px;
                color: #0088CC;
            }
            .author {
                font-weight: bold;
                color: #B7B7B7;
            }
            .blue_span {
                font-weight: bold;
                color: #0088CC;
            }
        }
    }

    .tags {
        width: 16%;
        margin-left: 50px;
        ul {
            padding: 0;
            display: flex;
            flex-wrap: wrap;
            li {
                list-style: none;
                text-transform: uppercase;
                font-size: 11px;
                border-radius: 5px;
                margin: 4px;
                padding: 5px;
                cursor: pointer;
                background-color: #000000;
                color: white;

                &:hover {
                    color: #0088CC;
                }
            }
        }
    }

    // label
    .label {
        font-family: 'Shadows Into Light', cursive;
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        top: 0;
        left: 17%;
        transform: translate(-58%, -50%);
        width: 150px;
        height: 50px;
        text-transform: capitalize;
        color: white;
        background-color: #0088CC ;

        &::before {
            position: absolute;
            top: 0;
            left: 0;
            transform: translate(-100%, 0%);
            content: "";
            width: 0;
            height: 0;
            border-style: solid;
            border-width: 0 0 25px 14px;
            border-color: transparent transparent #005580 transparent;
        }
    }


    // bottom footer
    .bottom_footer {
        height: 80px;
        background-color: #1c2023;

        .container_75 {
            height: 80px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .bottom_footer_left {
            display: flex;
            align-items: center;
        }

        img {
            height: 30px;
            margin-right: 30px;
        }

        ul {
            display: flex;
            li {
                list-style: none;
                margin: 0 10px; 
                font-size: 13px;
                cursor: pointer;
                color: #777777;

                &:hover {
                    color: #0088CC;
                }

                i {
                    font-size: 10px;
                    margin-right: 10px;
                }
            }
        }
    }
</style>
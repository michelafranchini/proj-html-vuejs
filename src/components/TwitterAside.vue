<template>
    <aside>
        <div class="twitter">
            <h3>Latest from twitter</h3>
            <div class="twitter_post">
                <i class="fab fa-twitter"></i>
                <div class="text">
                    <h5>If you have any suggestions for the next updates, let us know.</h5>
                    <p>01.05 PM Sep 18th</p>
                </div>
            </div>
            <div class="twitter_post">
                <i class="fab fa-twitter"></i>
                <div class="text">
                    <h5>We have just updated Porto Admin. Check the changelong for more information</h5>
                    <p>01.04 PM Sep 18th</p>
                </div>
            </div>
        </div>
        <div class="instagram">
            <h3>photos from instagram</h3>
            <div class="ig_post">
                <div 
                v-for="image, index in instagramImages"
                :key="index" class="ig_container">
                    <img :src="image.url" alt="">
                </div>
            </div>
        </div>
    </aside>
</template>

<script>
export default {
    name:"TwitterAside", 
    data() {
        return {
            instagramImages: [
                {
                link: "", 
                url: require("../assets/images/29739607_2020680068220520_4509928046932787200_n.jpg")
                },
                {
                link: "", 
                url: require("../assets/images/30087804_253872848488989_8792603541668626432_n.jpg")
                },
                {
                link: "", 
                url: require("../assets/images/29415620_196477127626244_3250318472361541632_n.jpg")
                },
                {
                link: "", 
                url: require("../assets/images/30078414_1274410412703843_8290935809419247616_n.jpg")
                },
                {
                link: "", 
                url: require("../assets/images/30077195_2066750973610181_3733150062893596672_n.jpg")
                },
                {
                link: "", 
                url: require("../assets/images/29415304_166583630713703_1032667922171953152_n.jpg")
                }, 
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
        h3 {
            font-size: 15px;
            text-transform: uppercase;
            color: black;
        }
        .twitter, 
        .instagram {
            margin-left: 30px;

            .twitter_post {
                display: flex;
                h5 {
                    line-height: 25px;
                    margin: 0;
                    color: #7d7d7d;
                }
                p {
                    font-size: 11px;
                    font-weight: bold;
                    color: #0088cc;
                }
                i {
                    margin-right: 20px;
                    font-size: 20px;
                    color: #212529;
                }
            }
        }
        .ig_post {
            display: flex;
            flex-wrap: wrap;
            justify-content: start;

            .ig_container {
                width: 33%;
                height: auto;
            }

            img {
                width: 100%;
            }
        }
</style>
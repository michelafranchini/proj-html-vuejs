<template>
    <section>
        <div class="container_75">
            <i class="fas fa-chevron-left" @click="prevTag"></i>
            <div class="container60" id="slider">
                <ul>
                    <li v-for="sliderTag, index in sliderTags"
                    :key="index">
                        {{sliderTag.tag}}
                    </li>
                </ul>
            </div>
            <i class="fas fa-chevron-right" @click="nextTag"></i>
        </div>
    </section>
</template>

<script>
export default {
    name: "Slider", 
    props: ["sliderTags"],
    data() {
        return
    }, 
    methods: {
        prevTag() {
            const cont = document.getElementById('slider'); 
            cont.scrollLeft -= 1390;
        }, 
        nextTag() {
            const cont = document.getElementById('slider'); 
            cont.scrollLeft += 1390;
        }
    }
}
</script>

<style lang="scss" scoped>
    section {
        height: 150px;
        background-color: #0088cc;

        .container_75 {
            width: 75%;
            height: 150px;
            margin: auto;
            display: flex;
            align-items: center;

            i {
                cursor: pointer;
            }
        }
    }
    ul {
        display: flex;
        flex-wrap: nowrap;
        margin: 0;
        padding: 0;
        
        li {
            width: 165px;
            list-style: none;
            text-transform: uppercase;
            margin: 25px;
            padding: 10px;
            font-size: 15px;
            text-align: center;
            cursor: pointer;
            background-color: #212529;
            color: white;

            &:hover {
                background-color: #32383e;
            }
            
        }

    }

    .container60 {
        width: 98%;
        height: 150px;
        margin: auto;
        display: flex;
        flex-wrap: no-wrap;
        align-items: center;
        overflow-x: scroll;

        &::-webkit-scrollbar {
                display: none;
            }
    }
</style>
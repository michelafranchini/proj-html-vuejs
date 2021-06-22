<template>
    <section>
        <div class="container_75">
            <i class="fas fa-chevron-left"></i>
            <ul>
                <li v-for="sliderTag, index in sliderTags"
                :key="index">
                    {{sliderTag.tag}}
                </li>
            </ul>
            <i class="fas fa-chevron-right"></i>
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

        }, 
        nextTag() {

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
        
        li {
            list-style: none;
            text-transform: uppercase;
            margin: 25px;
            padding: 10px;
            cursor: pointer;
            background-color: #212529;
            color: white;
            
        }

    }
</style>
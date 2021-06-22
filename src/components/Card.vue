<template>
  <div class="card_container">

        <img :src="card.url" alt="">
        <div class="description">
            <div class="calendar">
                <div class="calendar_day">
                    <span>{{card.calDay}}</span>
                </div>
                <div class="calendar_month">
                    <span>{{card.calMonth}}</span>
                </div>
            </div>
            <div>
                <h2>{{card.title}}</h2>
                <p>{{card.text}}</p>
                <div class="icons">
                    <div class="icons_left">
                        <i class="far fa-user"></i><h5> {{card.author}}</h5>
                        <i class="far fa-folder"></i><h5>{{card.tags}}</h5>
                        <i class="far fa-comment"></i><h5>{{card.comments}}</h5>
                    </div>
                    <h4>read more</h4>
                </div>
            </div>
        </div>
  </div>
</template>

<script>
export default {
    name: "Card", 
    props: ["card"]
}
</script>

<style lang="scss" scoped>
    .card_container {
        width: 1050px;
        margin: 50px 0;
    }
    img {
        width: 1050px;
    }

    .icons {
        display: flex;
        justify-content: space-between;
        border-bottom: 1px solid #f0f0f0;
    }

    .icons_left {
        display: flex;
        align-items: center;
        margin-bottom: 30px;

        h5 {
            margin: 0 10px;
            font-size: 12px;
            color: #0088cc;
        }
        i {
            font-size: 14px;
            color: #888888;
        }
    }

    p {
        line-height: 25px;
    }

    h2 {
        text-transform: capitalize;
        margin: 0;
    }

    h4 {
        cursor: pointer;
        display: inline-block;
        text-transform: uppercase;
        padding: 5px 7px;
        font-size: 10px;
        border: 1px solid #888888;
        border-radius: 5px;
        color: #888888;
    }

    .calendar {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin-right: 30px;

        span {
            font-size: 12px;
            font-weight: bold;
        }

        .calendar_day, 
        .calendar_month {
            width: 35px;
            display: flex;
            justify-content: center;
            align-items: center;

        }
        .calendar_day {
            height: 50px;
            background-color:#f7f7f7;
            color: #212529;
        }
        .calendar_month {
            background-color: #212529;
            color: #f7f7f7;
        }


    }

    .description {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        margin: 20px 0;
    }
    
</style>
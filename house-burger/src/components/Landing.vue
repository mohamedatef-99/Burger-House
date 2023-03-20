<template>
    <main :class="'d-flex justify-content-between'">
        <div :class="'head'">
            <p>{{ uppercaseDesName }}</p>
            <h1>{{ uppercaseBurger }}</h1>
            <h2>{{ uppercaseWeek }}</h2>
        </div>
        <div :class="'image d-flex'">
            <div :class="'discount position-absolute'">
                <h3>$5.<span>49</span></h3>
                <p>{{ uppercaseOnly }}</p>
            </div>
            <img :src="require('@/assets/images/main1.png')" alt="Burger Picture">
        </div>
    </main>
</template>

<script>
    export default {
    name: 'Body-app',
        data() {
            return {
                desName: 'it is a good time for the great taste of burgers',
                burger: 'burger',
                week: 'week',
                only: 'only'
            }   
        },
        computed: {
            uppercaseDesName() {
                return this.desName.toUpperCase()
            },
            uppercaseBurger() {
                return this.burger.toUpperCase()
            },
            uppercaseWeek() {
                return this.week.toUpperCase()
            },
            uppercaseOnly() {
                return this.only.toUpperCase()
            }
        }
    }
</script>

<style scoped>
    main{
        background-color: #ffba08b8;
        padding: 20px;
    }
    .head{
        margin-left: 15px;
        margin-top: 50px;
    }
    .head p{
        color: #99582a;
        font-size: 15px;
        border: 3px dashed #99582a;
        font-weight: bold;
        text-align: center;
        max-width: 450px;
    }
    .head h1{
        font-size: 120px;
        font-weight: 900;
        color: #4b250a;
    }
    .head h2{
        color: #4b250a;
        font-size: 70px;
        font-weight: 800;
    }
    .image img{
        max-width: 500px;
        height: 467px;
        margin-right: 15px;
    }
    .image .discount {
        position: relative;
        box-sizing: border-box;
        bottom: 13%;
        width: 100px;
        height: 100px;
        text-align: center;
        border-radius: 50%;
        background-color: #bd1010;
        z-index: 9999;
    }
    .image .discount::before {
        content: "";
        display: block;
        position: absolute;
        top: 3px;
        left: 3px;
        right: 3px;
        bottom: 3px;
        background-color: transparent;
        border-radius: inherit;
        border: 2px dashed white;
        z-index: -1;
    }
    .discount h3{
        color: white;
        font-size: 20px;
        padding-top: 10px;
        font-weight: bold;
    }
    .discount span{
        font-size: 15px;
    }
    .discount p{
        font-size: 20px;
        font-weight: bold;
        color: white;
        letter-spacing: 6px;
    }
    @media only screen and (max-width: 340px) {
        main{
            flex-direction: column;
        }
        .head h1{
            font-size: 55px;
            margin-bottom: 0;
        }
        .head h2{
            font-size: 30px;
        }
        .head p{
            max-width: 250px;
            font-size: 12px;
            margin-bottom: 0;
        }
        .image img{
            max-width: 310px;
            height: 400px;
            margin: 0 auto;
        }
        .image .discount{
            bottom: 28%;
            left: 20%;
            width: 90px;
            height: 90px;
            margin-right: 0;
        }
        .discount p{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 341px) and (max-width: 480px) {
        main{
            flex-direction: column;
        }
        .head h1{
            font-size: 65px;
            margin-bottom: 0;
        }
        .head h2{
            font-size: 40px;
        }
        .head p{
            max-width: 350px;
            font-size: 12px;
            margin-bottom: 0;
        }
        .image img{
            max-width: 340px;
            height: 400px;
            margin: 0 auto;
        }
        .image .discount{
            bottom: 28%;
            left: 20%;
            width: 90px;
            height: 90px;
            margin-right: 0;
        }
        .discount p{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 481px) and (max-width: 600px) {
        main{
            flex-direction: column;
        }
        .head h1{
            font-size: 70px;
            margin-bottom: 0;
        }
        .head h2{
            font-size: 40px;
        }
        .head p{
            max-width: 350px;
            font-size: 12px;
            margin-bottom: 0;
        }
        .image img{
            max-width: 340px;
            height: 400px;
            margin: 0 auto;
        }
        .image .discount{
            bottom: 0;
            left: 20%;
            width: 90px;
            height: 90px;
            margin-right: 0;
        }
        .discount p{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 601px) and (max-width: 768px) {
        
        .head h1{
            font-size: 50px;
            margin-bottom: 0;
        }
        .head h2{
            font-size: 30px;
        }
        .head p{
            max-width: 300px;
            font-size: 12px;
            margin-bottom: 30px;
        }
        .image img{
            max-width: 325px;
            height: 450px;
            margin-right: 0;
        }
        .image .discount{
            bottom: 18%;
            width: 90px;
            height: 90px;
        }
        .discount p{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 769px) and (max-width: 1024px) {
        .head h1{
            font-size: 80px;
        }
        .head h2{
            font-size: 60px;
        }
        .image img{
            max-width: 335px;
            height: 460px;
            margin-right: 0;
        }
        .image .discount{
            bottom: 18%;
        }
    }
</style>
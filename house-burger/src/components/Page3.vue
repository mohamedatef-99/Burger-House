<template>
    <main :class="''">
        <div :class="'container d-flex justify-content-between align-items-center'">
            <div :class="'head p-4 d-flex flex-column justify-content-start'">
                <h2>{{ uppercaseDiscover }}</h2>
                <h1>{{ uppercaseEvent }}</h1>
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Accusantium, quaerat eveniet distinctio ratione illo porro quibusdam facilis voluptates quidem corporis autem facere rerum reprehenderit fugiat adipisci iusto voluptatem quasi assumenda.</p>
                <div :class="'span d-flex mt-auto'">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </div>
            <img :src="require('@/assets/images/main5.jpg')" alt="Burger Picture" :class="'p-4'">
        </div>
    </main>
</template>

<script>
    export default {
    name: 'Page3-app',
    data() {
        return {
            discover: 'discover',
            event: 'upcoming events',
            }
    },
        computed:{
            uppercaseDiscover(){
                return this.discover.toUpperCase()
            },
            uppercaseEvent(){
                return this.event.toUpperCase()
            }
        }
    }
</script>

<style scoped>
    main{
        margin-top: 100px;
        margin-bottom: 100px;
    }
    .container{
        box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.5);
    }
    .head{
        width: 500px;
    }
    .head h2{
        color: #4b250a;
        font-size: 15px;
        font-weight: bold;
    }
    .head h1{
        color: #4b250a;
        font-size: 30px;
        font-weight: 900;
    }
    .head p{
        color: #4b250a;
        font-size: 13px;
    }
    .head .span{
        bottom: 0;
    }
    .head span{
        width: 10px;
        height: 10px;
        border-radius: 50%;
        margin-right: 5px;;
        background-color: rgb(160, 154, 154);
    }
    .head .span span:first-child{
        background-color: #ffba08;
    }
    main img{
        width: 500px;
        height: 300px;
    }
    @media only screen and (max-width: 340px) {
        .container{
            display: flex;
            flex-direction: column;
        }
        main img{
            width: 300px;
            height: 250px;
            padding: 10px !important;
        }
        .head{
            width: 350px;
            
        }
        .head h2{
            font-size: 12px;
        }
        .head h1{
            font-size: 17px;
        }
    }
    @media only screen and (min-width: 341px) and (max-width: 480px) {
        .container{
            display: flex;
            flex-direction: column;
        }
        main img{
            width: 300px;
            height: 250px;
            padding: 10px !important;
        }
        .head{
            width: 350px;
            
        }
        .head h2{
            font-size: 12px;
        }
        .head h1{
            font-size: 17px;
        }
    }
    @media only screen and (min-width: 481px) and (max-width: 768px) {
        main img{
            width: 230px;
            height: 250px;
            padding: 10px !important;
        }
        .head{
            width: 500px;
        }
        .head h2{
            font-size: 13px;
        }
        .head h1{
            font-size: 20px;
        }
    }
    @media only screen and (min-width: 769px) and (max-width: 1024px) {}
</style>
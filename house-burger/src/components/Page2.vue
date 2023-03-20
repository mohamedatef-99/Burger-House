<template>
    <main>
        <div :class="'head text-center'">
            <h2>{{ uppercaseTitle }}</h2>
            <h1>{{ uppercaseChoose }}</h1>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Explicabo sed illum reiciendis fugiat fuga, veniam minus ea temporibus et excepturi! Molestiae modi<br> necessitatibus perspiciatis, similique tempore iste libero iure temporibus!</p>
        </div>
        <div :class="'container text-center'">
            <div :class="'items row'">
                <div :class="'col-sm-12 col-md-4'">
                    <div :class="'item1'">
                        <img :src="require('@/assets/images/picture1.png')" alt="Burger Picture">
                        <div>
                            <h2>{{ uppercaseLorem }}</h2>
                            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.sed illum reiciendis</p>
                            <button>{{ uppercaseButton }}</button>
                        </div>
                    </div>
                </div>
                <div :class="'col-sm-12 col-md-4'">
                    <div :class="'item2'">
                        <img :src="require('@/assets/images/picture2.png')" alt="Burger Picture">
                        <div>
                            <h2>{{ uppercaseLorem }}</h2>
                            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.sed illum reiciendis</p>
                            <button>{{ uppercaseButton }}</button>
                        </div>
                    </div>
                </div>
                <div :class="'col-sm-12 col-md-4'">
                    <div :class="'item3'">
                        <img :src="require('@/assets/images/picture3.png')" alt="Burger Picture">
                        <div>
                            <h2>{{ uppercaseLorem }}</h2>
                            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.sed illum reiciendis</p>
                            <button>{{ uppercaseButton }}</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
    export default {
    name: 'Page-app',
    data() {
        return {
            title: 'always taste burger',
            choose: 'choose & enjoy',
            lorem: 'lorem ipsum dolor',
            button: 'order now',
            }
    },
    computed: {
        uppercaseTitle() {
                return this.title.toUpperCase()
        },
        uppercaseChoose() {
                return this.choose.toUpperCase()
        },
        uppercaseLorem() {
            return this.lorem.toUpperCase()
        },
        uppercaseButton() {
            return this.button.toUpperCase()
        },
        }
    }
</script>

<style scoped>
    main{
        margin-top: 50px;
        padding-top: 50px;
        margin-bottom: 50px;
    }
    main img{
        width: 270px;
        height: 270px;
        /*box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.5);*/
    }
    .container{
        margin-top: 50px;
    }
    .head h2{
        font-size: 15px;
        color: #4b250a;
        background-color: #ffba08;
        width: 200px;
        padding: 10px;
        margin: auto;
        font-weight: bold;
    }
    .head h1{
        font-size: 40px;
        color: #4b250a;
        font-weight: 900;
        padding-top: 20px;
    }
    .head p{
        padding: 20px;
    }
    .items h2{
        font-size: 20px;
        color: #4b250a;
        font-weight: bold;
        padding: 20px 0 10px;
    }
    .items p{
        font-size: 12px;
        color: #4b250a;
    }
    .items button{
        color: white;
        font-weight: bolder;
        background-color: rgb(177, 10, 10);
        padding: 10px;
        border-radius: 6px;
        border: none;
    }
    .items button:hover{
        opacity: 0.7;
    }
    @media only screen and (max-width: 340px) {
        main img{
            width: 170px;
            height: 170px;
        }
        .head h1{
            font-size: 20px;
        }
        .head h2{
            font-size: 12px;
        }
        .head p{
            font-size: 13px;
        }
        .item2, .item3{
            margin-top: 40px;
        }
        .items button{
            font-size: 13px;
        }
        .items h2{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 341px) and (max-width: 480px) {
        main img{
            width: 200px;
            height: 200px;
        }
        .head h1{
            font-size: 25px;
        }
        .head h2{
            font-size: 12px;
        }
        .head p{
            font-size: 13px;
        }
        .item2, .item3{
            margin-top: 40px;
        }
        .items button{
            font-size: 13px;
        }
        .items h2{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 481px) and (max-width: 768px) {
        main img{
            width: 250px;
            height: 250px;
        }
        .head h1{
            font-size: 30px;
        }
        .head h2{
            font-size: 13px;
        }
        .head p{
            font-size: 14px;
        }
        .item2, .item3{
            margin-top: 40px;
        }
    }
    @media only screen and (min-width: 769px) and (max-width: 1024px) {
        main img{
            width: 230px;
            height: 230px;
        }
    }
</style>
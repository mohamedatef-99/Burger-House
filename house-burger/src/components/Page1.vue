<template>
    <main>
        <div :class="'container d-flex justify-content-center align-items-center'">
            <div :class="'image1'">
                <div :class="'title d-flex flex-column'">
                    <h2>{{ uppercasepicDes1 }}</h2>
                    <h1>{{ uppercasepicDes2 }}</h1>
                </div>
                <img :src="require('@/assets/images/main3.jpg')" alt="Burger Picture">
            </div>
            <div :class="'image2 d-flex flex-column'">
                <div :class="'img1'">
                    <div :class="'title1 d-flex flex-column'">
                        <h2>{{ uppercasepicDes1 }}</h2>
                        <h1>{{ uppercasepicDes3 }}</h1><br>
                        <h1>{{ uppercasepicDes4 }}</h1>
                    </div>
                    <img :src="require('@/assets/images/main6.jpg')" alt="Burger Picture">
                </div>
                <div :class="'img2 mt-3'">
                    <div :class="'title2 d-flex flex-column'">
                        <h2>{{ uppercasepicDes1 }}</h2>
                        <h1>{{ uppercasepicDes5 }}</h1>
                    </div>
                    <img :src="require('@/assets/images/main5.jpg')" alt="Burger Picture">
                </div>
            </div>
        </div>
    </main>
</template>

<script>
    export default {
    name: 'Page-app',
    data() {
        return{
            picDes1: 'try it today',
            picDes2: 'most popular burger',
            picDes3: 'more fun',
            picDes4: 'more taste',
            picDes5: 'fresh & chill'
        }
    },
    computed: {
        uppercasepicDes1() {
                return this.picDes1.toUpperCase()
        },
        uppercasepicDes2() {
                return this.picDes2.toUpperCase()
            },
        uppercasepicDes3() {
                return this.picDes3.toUpperCase()
        },
        uppercasepicDes4() {
                return this.picDes4.toUpperCase()
        },
        uppercasepicDes5() {
                return this.picDes5.toUpperCase()
            }
        }
    }
</script>

<style scoped>
    .container{
        margin-top: 50px;
        padding-top: 50px;
        padding-bottom: 50px;
        margin-bottom: 50px;
    }
    .image1 {
        margin-right: 30px;
    }
    .image1 img{
        width: 500px;
        height: 420px;
        border-radius: 10px;
    }
    .image2 img{
        width: 500px;
        height: 200px;
        border-radius: 10px;
    }
    .title,
    .title1,
    .title2{
        position: absolute;
        padding: 20px;
    }
    .image1 h1,
    .image1 h2,
    .img1 h1,
    .img1 h2,
    .img2 h1,
    .img2 h2 {
    color: white;
    z-index: 1;
    }
    .image1 h1,
    .img1 h1,
    .img2 h1{
        font-size: 20px;
        font-weight: bold;
    }
    .image1 h2,
    .img1 h2,
    .img2 h2{
        font-size: 15px;
        font-weight: bold;
    }
    @media only screen and (max-width: 340px) {
        .title,
        .title1,
        .title2{
            padding: 20px 5px;
        }
        .image1 {
            margin-right: 15px;
        }
        .image1 img{
            width: 150px;
            height: 220px;
        }
        .image2 img{
            width: 150px;
            height: 100px;
        }
        .image1 h1,
        .img1 h1,
        .img2 h1{
            font-size: 12px;
        }
        .image1 h2,
        .img1 h2,
        .img2 h2{
            font-size: 10px;
        }
    }
    @media only screen and (min-width: 341px) and (max-width: 480px) {
        .title,
        .title1,
        .title2{
            padding: 20px 5px;
        }
        .image1 {
            margin-right: 15px;
        }
        .image1 img{
            width: 170px;
            height: 220px;
        }
        .image2 img{
            width: 170px;
            height: 100px;
        }
        .image1 h1,
        .img1 h1,
        .img2 h1{
            font-size: 13px;
        }
        .image1 h2,
        .img1 h2,
        .img2 h2{
            font-size: 10px;
        }
    }
    @media only screen and (min-width: 481px) and (max-width: 600px) {
        .image1 img{
            width: 200px;
            height: 320px;
        }
        .image2 img{
            width: 200px;
            height: 150px;
        }
        .image1 h1,
        .img1 h1,
        .img2 h1{
            font-size: 15px;
        }
        .image1 h2,
        .img1 h2,
        .img2 h2{
            font-size: 12px;
        }
    }
    @media only screen and (min-width: 601px) and (max-width: 768px) {
        .image1 img{
            width: 280px;
            height: 320px;
        }
        .image2 img{
            width: 280px;
            height: 150px;
        }
        .image1 h1,
        .img1 h1,
        .img2 h1{
            font-size: 17px;
            font-weight: bold;
        }
        .image1 h2,
        .img1 h2,
        .img2 h2{
            font-size: 13px;
            font-weight: bold;
        }
    }
    @media only screen and (min-width: 769px) and (max-width: 1024px) {
        .image1 img{
            max-width: 350px;
        }
        .image2 img{
            width: 350px;
        }
    }
</style>
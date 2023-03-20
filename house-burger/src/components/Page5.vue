<template>
    <main>
        <div :class="'e position-relative'">
            <div :class="'cover-img'">
                <img :src="require('@/assets/images/cover.jpg')" alt="Burger Picture">
            </div>
            <div :class="'containere d-flex flex-column justify-content-between'">
                <div :class="'title d-flex mt-4'">
                    <i class="fa-solid fa-burger"></i>
                    <h1>{{ uppercaseBurger }}</h1>
                </div>
                <div :class="'details d-flex justify-content-between align-items-center mt-5'">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. A impedit fugit aliquid molestias nesciunt quasi, ea doloribus vitae, distinctio veniam quas adipisci voluptates, quaerat reprehenderit illo aut? Doloremque, ullam eos.</p>
                    <div :class="'det-icon d-flex flex-column'">
                        <div :class="'d-flex align-items-center'">
                            <i class="fa-solid fa-location-dot"></i>
                            <span>MAIN ROAD.BUILDING NAME.COUNTRY</span>
                        </div>
                        <div :class="'d-flex align-items-center'">
                            <i class="fa-solid fa-envelope"></i>
                            <span>INFO@COMPANY.COM</span>
                        </div>
                    </div>
                </div>
                <div :class="'copy-rights d-flex mt-4 justify-content-between align-items-center'">
                    <span>&copy; {{ uppercaseCompany }}</span>
                    <div :class="'icons d-flex flex-row '">
                        <i class="fa-brands fa-instagram"></i>
                        <i class="fa-brands fa-facebook"></i>
                        <i class="fa-brands fa-twitter"></i>
                        <i class="fa-brands fa-whatsapp"></i>
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
            burger: 'burger house',
            company: 'company name 2020 all rights reserved'
            }
    },
    computed: {
        uppercaseBurger() {
                return this.burger.toUpperCase()
        },
        uppercaseCompany() {
                return this.company.toUpperCase()
            }
        }
    }
</script>

<style scoped>
.e{
    padding: 30px;
}
    .cover-img {
    position: relative;
    width: 100%;
    height: 100%;
}
    .cover-img img {
        position: relative;
        top: 0;
        left: 0;
        width: 100%;
        height: 400px;
        object-fit: cover;
}
    .cover-img::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(9, 5, 5, 0.74);
        z-index: 1;
    }
    .containere{
        position: absolute;
        top:0;
        width: calc(100% - 50px);
        height: 400px;
        padding: 50px;
        z-index: 2;
    }
    .title i{
        color: white;
        font-size: 40px;
        margin-right: 10px;
    }
    .title h1{
        font-size: 34px;
        font-weight: 900;
        color: white;
    }
    .details p{
        color: white;
        font-size: 15px;
        width: 500px;
    }
    .details i{
        color: white;
        font-size: 25px;
        padding: 10px;
    }
    .details span{
        color: white;
        font-size: 20px;
        margin-left: 15px;
    }
    .copy-rights{
        margin-top: auto;
        position: relative;
        bottom: -50px;
    }
    .copy-rights span{
        font-size: 15px;
        color: white;
    }
    .copy-rights i{
        color: black;
        font-size: 20px;
        background-color: white;
        border-radius: 50%;
        width: 30px;
        height: 30px;
        text-align: center;
        justify-content: center;
        align-items: center;
        margin-left: 10px;
        display: flex;
        cursor: pointer;
    }
    .copy-rights i:hover{
        opacity: 0.7;
    }
    @media only screen and (max-width: 340px) {
        .containere {
            padding: 30px 20px;
        }
        .title i{
            font-size: 25px;
        }
        .title h1{
            font-size: 20px;
        }
        .details{
            margin-top: 15px !important;
            flex-direction: column;
        }
        .details p{
            font-size: 11px;
            width: 250px;
        }
        .details i{
            font-size: 15px;
        }
        .details span{
            font-size: 11px;
        }
        .copy-rights span{
            font-size: 10px;
        }
        .copy-rights i{
            width: 20px;
            height: 20px;
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 341px) and (max-width: 480px) {
        .containere {
            padding: 30px 20px;
        }
        .title i{
            font-size: 25px;
        }
        .title h1{
            font-size: 20px;
        }
        .details{
            margin-top: 15px !important;
            flex-direction: column;
        }
        .details p{
            font-size: 11px;
            width: 250px;
        }
        .details i{
            font-size: 15px;
        }
        .details span{
            font-size: 11px;
        }
        .copy-rights span{
            font-size: 10px;
        }
        .copy-rights i{
            width: 20px;
            height: 20px;
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 481px) and (max-width: 600px) {
        .title i{
            font-size: 25px;
        }
        .title h1{
            font-size: 20px;
        }
        .details{
            margin-top: 15px !important;
        }
        .details p{
            font-size: 11px;
        }
        .details i{
            font-size: 15px;
        }
        .details span{
            font-size: 11px;
        }
        .copy-rights span{
            font-size: 10px;
        }
        .copy-rights i{
            width: 20px;
            height: 20px;
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 601px) and (max-width: 768px) {
        .title i{
            font-size: 30px;
        }
        .title h1{
            font-size: 25px;
        }
        .details p{
            font-size: 13px;
        }
        .details i{
            font-size: 20px;
        }
        .details span{
            font-size: 13px;
        }
        .copy-rights span{
            font-size: 11px;
        }
    }
    @media only screen and (min-width: 769px) and (max-width: 1024px) {}
</style>
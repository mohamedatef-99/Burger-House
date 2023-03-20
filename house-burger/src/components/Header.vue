<template>
    <header>
        <div :class="'logo d-flex justify-content-between'">
            <div :class="'logo-r d-flex'">
                <i class="fa-solid fa-burger"></i>
                <h3>{{ uppercaseLogoName }}</h3>
            </div>
            <div :class="'logo-l d-flex'">
                <i class="fa-solid fa-truck"></i>
                <h3>Express Delivery +1 234 567 890</h3>
            </div>
        </div>
        <nav :class="'d-flex justify-content-end'">
            <ul class="my-nav d-flex flex-end" :class="{ active: isOpen }">
                <li><a :href="homeLink">{{ uppercaseHomeLink }}</a></li>
                <li><a :href="menuLink">{{ uppercaseMenuLink }}</a></li>
                <li><a :href="storyLink">{{ uppercaseStoryLink }}</a></li>
                <li><a :href="contactLink">{{ uppercaseContactLink }}</a></li>
            </ul>
            <div :class="'burger-menu d-none'" @click="isOpen = !isOpen">
                <i class="fa-solid fa-bars"></i>
            </div>
        </nav>
    </header>
</template>

<script>
// import '@fortawesome/fontawesome-free/css/all.css'
    export default {
    name: 'Header-app',
        data() {
            return {
                logoName: "burger house",
                homeLink: "home",
                menuLink: "menu",
                storyLink: "our story",
                contactLink: "contact us",
                isOpen: false,
            }
    },
    computed: {
            uppercaseLogoName() {
                return this.logoName.toUpperCase()
            },
            uppercaseHomeLink() {
                return this.homeLink.toUpperCase()
            },
            uppercaseMenuLink() {
                return this.menuLink.toUpperCase()
            },
            uppercaseStoryLink() {
                return this.storyLink.toUpperCase()
            },
            uppercaseContactLink() {
                return this.contactLink.toUpperCase()
            },
    },
}

</script>

<style scoped>
    header{
        padding: 20px;
        background-color: #ffba08b8;
    }
    .logo-r{
        padding-left: 15px;
    }
    .logo-r i{
        font-size: 30px;
        color: black;
        margin-right: 10px;
    }
    .logo-r h3{
        font-size: 25px;
        color: black;
        font-weight: bold;
    }
    .logo-l{
        padding-right: 15px;
    }
    .logo-l i{
        font-size: 20px;
        color: black;
        margin-right: 10px;
    }
    .logo-l h3{
        font-size: 15px;
        color: black;
    }
    nav ul{
        list-style: none;
        margin-right: 15px;
    }
    nav a{
        text-decoration: none;
        color: black;
        font-size: 15px;
        font-weight: bold;
        margin-left: 30px;
    }
    nav a:hover{
        opacity: 0.7;
    }
    .burger-menu{
        z-index: 99999;
        font-size: 25px;
        margin-right: 15px;
        cursor: pointer;
    }
    @media only screen and (max-width: 480px) {
        nav ul{
            flex-direction: column;
            text-align: center;
            justify-content: center;
            background-color: #bb3e03;
            width: 100%;
            height: 100%;
            top: 0;
            right: 0;
            position: absolute;
            transition: transform 0.5s ease-in-out;
            z-index: 99999;
            margin-right: 0;
            transform: translateY(-100%) ;
            padding: 0;
        }
        nav li{
            margin-top: 50px;
            text-align: center;
        }
        nav a {
            color: white;
        }
        .burger-menu{
            display: block !important;
        }
        .burger-menu i{
            top: 25px;
            position: absolute;
        }
        nav ul.active{
            transform: translateY(0) ;
        }
        .logo-r h3{
            font-size: 20px;
            padding-top: 5px;
        }
        .logo-r i{
            font-size: 30px;
        }
        .logo-l{
            display: none !important;
        }
    }
    @media only screen and (min-width: 481px) and (max-width: 768px) {
        nav ul{
            flex-direction: column;
            text-align: center;
            justify-content: center;
            background-color: #bb3e03;
            width: 50%;
            height: 100%;
            top: 0;
            right: 0;
            position: absolute;
            transition: transform 0.5s ease-in-out;
            z-index: 99999;
            margin-right: 0;
            transform: translateY(-100%) ;
            display: none;
            padding: 0;
        }
        nav li{
            margin-top: 50px;
            text-align: center;
        }
        nav a {
            color: white;
        }
        .burger-menu{
            display: block !important;
        }
        nav ul.active{
            transform: translateY(0) ;
        }
        .logo-r h3{
            font-size: 15px;
        }
        .logo-r i{
            font-size: 20px;
        }
        .logo-l h3{
            font-size: 12px;
        }
        .logo-l i{
            font-size: 15px;
        }
    }
</style>
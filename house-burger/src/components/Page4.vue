<template>
    <main>
        <!-- <div>
            <pre>
                {{ JSON.stringify(formData, null, 2) }}
            </pre>
        </div> -->
        <div :class="'img1 position-relative'">
            <img :src="require('@/assets/images/pic1.png')" alt="Burger Picture">
        </div>
        <div :class="'container position-relative'">
            <div :class="'head text-center'">
                <h2>{{ uppercaseReserve }}</h2>
                <h1>{{ uppercaseBook }}</h1>
            </div>
            <div :class="'book d-flex align-items-center position-relative mt-5'">
                <img :src="require('@/assets/images/pic3.png')" alt="Burger Picture" :class="'img2'">
                <form :class="'reservation d-flex '" @submit="submitForm">
                    <div :class="'left'">
                        <div :class="'form-group position-relative'">
                            <label for="name" :class="{ active: isNameActive }">NAME</label>
                            <input type="text" id="name" v-model="formData.name" @focus="isNameActive = true" @blur="isNameActive = formData.name !== ''"/>
                        </div>
                        <div :class="'form-group position-relative mt-3'">
                            <label for="date" :class="{ active: isDataActive }">DATE</label>
                            <input type="text" id="date" v-model="formData.date" @focus="isDataActive = true" @blur="isDataActive = formData.date !== ''"/>
                        </div>
                        <div :class="'form-group position-relative mt-3'">
                            <label for="people" :class="{ active: isPeopleActive }">PEOPLE</label>
                            <input type="text" id="people" v-model="formData.people" @focus="isPeopleActive = true" @blur="isPeopleActive = formData.people !== ''"/>
                        </div>
                    </div >
                    <div :class="'right'">
                        <div :class="'form-group position-relative'">
                            <label for="email" :class="{ active: isEmailActive }">EMAIL</label>
                            <input type="email" id="email" v-model="formData.email" @focus="isEmailActive = true" @blur="isEmailActive = formData.email !== ''"/>
                        </div>
                        <div :class="'form-group position-relative mt-3'">
                            <label for="time" :class="{ active: isTimeActive }">TIME</label>
                            <input type="text" id="time" v-model="formData.time" @focus="isTimeActive = true" @blur="isTimeActive = formData.time !== ''"/>
                        </div>
                        <button :class="'mt-3'">{{ uppercaseTable }}</button>
                    </div>
                </form>
            </div>
        </div>
        <div :class="'img3 position-relative'">
            <img :src="require('@/assets/images/pic2.png')" alt="Burger Picture">
        </div>
    </main>
</template>

<script>
export default {
    name: 'Page4-app',
    data() {
        return {
            reserve: "reservation",
            book: 'book your table',
            table: 'find a table',
            formData: {
                name: '',
                email: '',
                date: '',
                time: '',
                people: '',
            },
            isNameActive: false,
            isDataActive: false,
            isPeopleActive: false,
            isTimeActive: false,
            isEmailActive: false,
        }
    },
    computed: {
        uppercaseReserve() {
            return this.reserve.toUpperCase()
        },
        uppercaseBook() {
            return this.book.toUpperCase()
        },
        uppercaseTable() {
            return this.table.toUpperCase()
        }
    },
    methods: {
        submitForm(event) {
            event.preventDefault();
            alert(`Form Data is: ${JSON.stringify(this.formData, null, 2)}`);
        }
    }
}
</script>

<style scoped>
    main{
        margin-top: 200px;
        margin-bottom: 50px;
    }
    .head h2{
        font-size: 15px;
        font-weight: bolder;
        color: #4b250a;
    }
    .head h1{
        font-size: 35px;
        font-weight: 900;
        color: #4b250a;
    }
    .img1 img{
        width: 200px;
        position: absolute;
        top: -30px;
        left: -30px;
    }
    .book img{
        width: 200px;
    }
    .form-group input{
        width: 350px;
        padding: 8px;
        border-radius: 6px;
        border: 1px solid #ccc;
    }
    .form-group label{
        position: absolute;
        top: 50%;
        left: 10px;
        transform: translateY(-50%);
        font-weight: bold;
        background-color: white;
        transition: all 0.2s ease-in-out;
    }
    .form-group label.active {
        top: 0;
        left: 10px;
        font-size: 17px;
    }

    .right{
        margin-left: 15px;
    }
    .right button{
        padding: 8px;
        background-color: red;
        color: white;
        font-size: 15px;
        font-weight: 900;
        border-radius: 6px;
        border: none;
        width: 350px;
    }
    .right button:hover{
        opacity: 0.7;
    }
    .img2{
        height: 200px;
    }
    .img3 img{
        width: 150px;
        position: absolute;
        right: 0;
        bottom: -30px;   
    }
    @media only screen and (max-width: 340px) {
        .reservation{
            flex-direction: column;
        }
        .right{
            margin: 15px 0;
        }
        .head h1{
            font-size: 20px;
        }
        .img3 img{
            display: none;
        }
        .form-group input{
            width: 170px;
        }
        .right button{
            width: 170px;
        }
        .img1 img{
            display: none;
        }
        .book img{
            height: 230px;
            width: 110px;
        }
        .form-group label{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 341px) and (max-width: 480px) {
        .reservation{
            flex-direction: column;
        }
        .right{
            margin: 15px 0;
        }
        .head h1{
            font-size: 25px;
        }
        .img3 img{
            display: none;
        }
        .form-group input{
            width: 200px;
        }
        .right button{
            width: 200px;
        }
        .img1 img{
            display: none;
        }
        .book img{
            height: 230px;
            width: 110px;
        }
        .form-group label{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 481px) and (max-width: 600px) {
        .reservation{
            flex-direction: column;
        }
        .right{
            margin: 15px 0;
        }
        .head h1{
            font-size: 25px;
        }
        .img3 img{
            display: none;
        }
        .form-group input{
            width: 230px;
        }
        .right button{
            width: 230px;
        }
        .img1 img{
            display: none;
        }
        .book img{
            height: 230px;
            width: 130px;
        }
        .form-group label{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 601px) and (max-width: 768px) {
        .head h1{
            font-size: 25px;
        }
        .img3 img{
            display: none;
        }
        .form-group input{
            width: 200px;
        }
        .right button{
            width: 200px;
        }
        .img1 img{
            width: 150px;
        }
        .book img{
            height: 180px;
            width: 120px;
        }
        .form-group label{
            font-size: 15px;
        }
    }
    @media only screen and (min-width: 769px) and (max-width: 1024px) {
        .head h1{
            font-size: 30px;
        }
        .img3 img{
            display: none;
        }
        .form-group input{
            width: 260px;
        }
        .right button{
            width: 260px;
        }
        .img1 img{
            width: 150px;
        }
        .book img{
            height: 180px;
        }
    }
</style>
<template>
    <div class="grid-container">
        <div class="grid-item item1"></div>
        <div class="grid-item item2"></div>
        <div class="grid-item item3"></div>
        <div class="grid-item item4"></div>
        <div class="grid-item item5"></div>
        <div class="grid-item item6 position-relative">
            <div class="icon-pizza">
                <img src="/public/svg/svg-4.svg" alt="" class="icon-pizza-img">
            </div>
        </div>
        <div class="grid-item item7"></div>
        <div class="grid-item item8"></div>
        <div class="grid-item item9"></div>
    </div>
    <div class="container">
        <div class="row">
            <div class="col-25 position-relative" v-for="img, index in teamImgs" :key="index">
                <img :src="img.src" alt="" class="team-img">
                <div class="icon-pizza" v-show="index == 3">
                    <img src="/public/svg/svg-4.svg" alt="" class="icon-pizza-img">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            teamImgs: [
                {
                    nome: '',
                    src: '/public/img/h1-team-1a-700x700.jpg',
                    ruolo: ''
                },
                {
                    nome: 'FRANK BAILEY',
                    src: '/public/img/h1-team-2a.jpg',
                    ruolo: 'Kitchen Porter'
                },
                {
                    nome: '',
                    src: '/public/img/h1-team-4a.jpg',
                    ruolo: ''
                },
                {
                    nome: '',
                    src: '/public/img/h1-team-3a.jpg',
                    ruolo: ''
                },
            ]
        }
    }
}
</script>

<style scoped>
    .grid-container {
        display: grid;
        grid-template-columns: 5% 90% 5%;
        grid-template-rows: 20% 60% 20%;
        width: 100%;
        height: 200px;
        margin-bottom: 5px;
    }

    .grid-item {
        background-image: url('/public/img/h3-background-img.jpg');
        background-size: cover;
        background-repeat: no-repeat;
    }

    .item1 {
        background-position: 100% 200%;
    }
    .item2 {
        background-position: 50% 100%;
    }
    .item3 {
        background-position: 100% 0%;
    }
    .item4 {
        background-position: 100% 100%;
    }
    .item5 {
        background-position: 0% 1%;
    }
    .item6 {
        background-position: 0% 0%;
    }
    .item7 {
        background-position: 20% 50%;
    }
    .item8 {
        background-position: 60% 60%;
    }
    .item9 {
        background-position: 100% 100%;
    }

    .team-img {
        width: 100%;
        height: auto;
    }
</style>
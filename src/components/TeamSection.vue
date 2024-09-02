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
        <h1 class="text-white">GO AHEAD AND BUILD YOUR OWN PIZZA WE WON'T JUDGE!</h1>
    </div>
    <div class="container">
        <div class="row">
            <div class="col-25 position-relative" v-for="img, index in teamImgs" :key="index">
                <div class="image-wrapper">
                    <img :src="img.src" :alt="img.nome" class="team-img">
                    <div class="overlay">
                        <h3 class="text-white fs-14">{{ img.nome }}</h3>
                        <p class="text-white fs-8">{{ img.ruolo }}</p>
                        <div class="text-white fs-8 social">
                            <i v-for="(icon, index) in socialIcons" :key="index" :class="`fa-brands ${icon} text-white fs-8`"></i>
                        </div>
                    </div>
                </div>
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
                    nome: 'Mario Rossi',
                    src: '/public/img/h1-team-1a-700x700.jpg',
                    ruolo: 'Chef'
                },
                {
                    nome: 'Frank Bailey',
                    src: '/public/img/h1-team-2a.jpg',
                    ruolo: 'Kitchen Porter'
                },
                {
                    nome: 'Luigi Bianchi',
                    src: '/public/img/h1-team-4a.jpg',
                    ruolo: 'Pizzaiolo'
                },
                {
                    nome: 'Anna Verdi',
                    src: '/public/img/h1-team-3a.jpg',
                    ruolo: 'Manager'
                },
            ],
            socialIcons: [
                'fa-twitter',
                'fa-facebook-f',
                'fa-square-instagram',
                'fa-linkedin-in'
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
        position: relative;
    }

    h1 {
        position: absolute;
        top: 17%;
        left: 20%;
        width: 20%;
        font-size: 26px;
        line-height: 1;
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

    .image-wrapper {
        position: relative;
        width: 100%;
    }

    .team-img {
        width: 100%;
        height: auto;
        transition: opacity 0.3s ease;
    }

    .overlay {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 90%;
        height: 90%;
        background-color: var(--bg-button);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        opacity: 0;
        transition: opacity 0.3s ease;
    }

    .image-wrapper:hover .team-img {
        opacity: 0;
    }

    .image-wrapper:hover .overlay {
        opacity: 1;
    }

    .social {
        margin-top: 10px;
    }

    i {
        margin: 0px 5px;
    }
</style>
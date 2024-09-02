<template>
    <div class="container position-relative">
        <div class="row">
            <div class="col-100 text-center position-relative">
                <div class="fs-10 text-danger my-10">CHOOSE YOUR FLAVOR</div>
                <h1 class="fs-20 my-10">THE BEST PIZZA MENU IN TOWN</h1>
                <p class="fs-12 text-warning">Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo voluptates accusamus earum magnam nam consequatur.</p>
                <div class="icon-pizza">
                    <img src="/public/svg/svg-4.svg" alt="" class="icon-pizza-img">
                </div>
            </div>
            <div class="col-100">
                <ul class="list-unstyled d-flex justify-content-center">
                    <li v-for="pizza,index in menuPizza" :key="index" class="text-center position-relative">
                        <img :src="pizza.src" alt="">
                        <div class="text-tertiary">{{ pizza.nome }}</div>
                        <div class="text-danger"><span v-show="pizza.costo_minimo">{{ pizza.costo_minimo }} - </span>{{ pizza.costo_massimo }}</div>
                        <div class="badge-sold" v-show="pizza.sold">
                            <span class="text-white fs-10">SOLD</span>
                        </div>
                    </li>
                </ul>
            </div>
            <div class="square">
                <img src="/public/svg/svg-10.svg" alt="">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            menuPizza: [
                {
                    nome: 'BISMARCK',
                    src: '/public/img/h3-product-img-1a-100x100.png',
                    sold: false,
                    costo_minimo: '$5.00',
                    costo_massimo: '$30.00'
                },
                {
                    nome: 'FIORI DI ZUCCA',
                    src: '/public/img/h3-product-img-2a-150x150.png',
                    sold: false,
                    costo_minimo: '$7.00',
                    costo_massimo: '$50.00'
                },
                {
                    nome: 'VALDOSTANA',
                    src: '/public/img/h3-product-img-3a-150x150.png',
                    sold: true,
                    costo_minimo: '',
                    costo_massimo: '$55.00'
                },
                {
                    nome: 'PIZZA TARTUFATA',
                    src: '/public/img/h3-product-img-4a-150x150.png',
                    sold: false,
                    costo_minimo: '',
                    costo_massimo: '$45.00'
                },
                {
                    nome: 'FRANCESCANA',
                    src: '/public/img/h3-product-img-5a-150x150.png',
                    sold: false,
                    costo_minimo: '',
                    costo_massimo: '$25.00'
                },
                {
                    nome: 'CAMPAGNOLA',
                    src: '/public/img/h3-product-img-6a-100x100.png',
                    sold: false,
                    costo_minimo: '$50.00',
                    costo_massimo: '$95.00'
                },
            ]
        }
    }
}
</script>

<style scoped>
    .col-100 {
        margin: 30px 0px;
    }

    ul {
        margin-bottom: 50px;
    }

    ul:hover {
        overflow-x: auto;
    }

    li {
        margin: 0px 30px;
    }

    li img {
        width: 150px;
        height: auto;
    }

    .badge-sold {
        position: absolute;
        top: 0;
        right: 10px;
        background-color: var(--bg-button);
        border-radius: 50%;
        width: 40px;
        height: 40px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .square {
        width: 30px;
        height: 30px;
        background-color: var(--bg-tertiary);
        position: absolute;
        bottom: 0;
        right: 0;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .square img {
        width: 15px;
        height: auto;
    }
</style>
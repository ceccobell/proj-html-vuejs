<template>
    <div class="container">
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
                <ul class="list-unstyled d-flex">
                    <li v-for="pizza,index in menuPizza" :key="index" class="text-center">
                        <img :src="pizza.src" alt="">
                        <div class="text-tertiary">{{ pizza.nome }}</div>
                        <div class="text-danger">{{ pizza.costo_massimo }}</div>
                    </li>
                </ul>
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

    li img {
        width: 150px;
        height: auto;
    }
</style>
<template>
    <div class="container">
        <div class="row">
            <div class="container-img">
                <img src="/public/img/h1-img-4.jpg" alt="" class="bg-img">
                <img src="/public/img/h1-img-7n.png" alt="" class="featured-img">
            </div>
            <div class="col-50 d-flex align-items-center justify-content-center">
                <div class="content">
                    <h1 class="fs-20">SPECIALS*</h1>
                    <p class="fs-12">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesent ut.</p>
                    <ul class="list-unstyled">
                        <li v-for="pizza,index in pizzas" :key="index" class="d-flex">
                            <div class="price fs-14">{{ pizza.prezzo }}</div>
                            <div>
                                <div class="nome-pizza fs-14">{{ pizza.nome }}</div>
                                <p class="fs-12">{{ pizza.descrizione }}</p>
                            </div>
                        </li>
                    </ul>
                    <div class="icon-pizza">
                        <img src="/public/svg/svg-4.svg" alt="">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        pizzas: Array
    }
}
</script>

<style scoped>
    .container-img {
        padding: 5px 0px;
    }

    .content {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        position: relative;
    }

    h1, p, ul {
        width: 70%; /* Fai sì che gli elementi occupino tutta la larghezza disponibile */
        text-align: left; /* Allinea il testo a sinistra */
    }

    .content p {
        color: var(--text-warning);
    }

    .price {
        color: var(--text-more-danger);
        font-weight: 600;
        margin-right: 10px;
    }
    
    ul {
        margin-top: 20px;
    }

    li {
        margin-bottom: 15px;
    }

    .nome-pizza {
        font-weight: 600;
        margin-bottom: 7px;
    }
</style>
<template>
    <div class="container">
        <div class="row">
            <div class="col-50 bg-cielostellato d-flex align-items-center justify-content-center">
                <div class="content">
                    <div class="fs-10 text-danger first-div">MADE WITH LOVE</div>
                    <h1 class="fs-20 text-white">DELISH PIZZA DEALS</h1>
                    <ul class="list-unstyled">
                        <li v-for="deal,index in pizzaDeals" :key="index" class="d-flex">
                            <div class="text-center m-end">
                                <div class="text-danger fs-24">{{ deal.giorno }}</div>
                                <div class="text-white fs-14">{{ deal.mese }}</div>
                            </div>
                            <div>
                                <div class="text-white fs-14">{{ deal.offer }}</div>
                                <div class="text-danger fs-10">{{ deal.dove }}</div>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="col-50 position-relative">
                <img src="/public/img/h3-img-5a.jpg" alt="" class="comic-img">
                <div class="icon-pizza">
                    <img src="/public/svg/svg-4.svg" alt="" class="icon-pizza-img">
                </div>
                <div class="square">
                    <img src="/public/svg/svg-9.svg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            pizzaDeals: [
                {
                    giorno: '02',
                    mese: 'NOV',
                    dove: '204 E. Pizzetta Tommaso',
                    offer: 'TRADITIONAL NEAPOLITAN PIES IN KYOTO PIZZA MERCATO'
                },
                {
                    giorno: '03',
                    mese: 'NOV',
                    dove: '204 E. Pizzetta Tommaso',
                    offer: 'TERRAZZA PATIO DINING SPACE OPENING THIS WEEKEND'
                },
                {
                    giorno: '05',
                    mese: 'NOV',
                    dove: '204 E. Pizzetta Tommaso',
                    offer: 'SIENNA PRIVATE DINING ROOM WITH STÈPHANE BRUNN'
                },
            ]
        }
    }
}
</script>

<style scoped>
    .container {
        margin-top: 5px
    }

    .bg-cielostellato {
        background-image: url(/public/img/cielostellato.PNG);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
    }

    .content {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        position: relative;
    }

    .content h1, .first-div, .content ul {
        width: 80%; 
        text-align: left; 
    }

    li {
        padding: 20px 0px;
    }

    li:nth-child(2) {
        border-top: 1px dashed #FFA323;
        border-bottom: 1px dashed #FFA323;
    }

    .m-end {
        margin-right: 20px;
    }

    .comic-img {
        width: 100%;
        height: auto;
    }

    .icon-pizza {
        top: 10px;
    }

    .square {
        width: 20px;
        height: 20px;
        background-color: white;
        position: absolute;
        top: 0;
        right: 0;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .square img {
        width: 10px;
        height: auto;
    }
</style>
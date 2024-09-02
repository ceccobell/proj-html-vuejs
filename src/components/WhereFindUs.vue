<template>
    <div class="container">
        <div class="row">
            <div class="col-50">

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
    
}
</script>

<style scoped>
    .container {
        margin-top: 5px
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
<template>
    <div class="container">
        <div class="row">
            <div class="col-25" v-for="image, index in images" :key="index">
                <div class="card">
                    <img :src="image.src" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        images: Array
    }
}
</script>

<style>
    .card {
        padding: 5px 5px 5px 0px;
    }

    .row div:last-child .card {
        padding: 5px 0px;
    }

    img {
        width: 100%;
        height: auto;
    }
</style>
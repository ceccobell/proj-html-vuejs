<template>
    <div class="container">
        <div class="row">
            <div class="col-25" v-for="image, index in images" :key="index">
                <div class="card">
                    <div class="image-wrapper">
                        <img :src="image.src" alt="" class="img-hovered">
                        <div class="overlay">
                            <div class="circle">
                                <img src="/public/svg/eye-svgrepo-com.svg" alt="">
                            </div>
                        </div>
                    </div>
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

<style scoped>
    .card {
        padding: 5px 5px 0px 0px;
    }

    .row div:last-child .card {
        padding: 5px 0px 0px 0px;
    }

    img {
        width: 100%;
        height: auto;
        transition: opacity 0.3s ease;
    }

    .overlay {
        background-color: white;
    }

    .circle {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background-color: var(--bg-button);
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .circle img {
        width: 30px;
        height: auto;
    }
</style>
<template>
    <div class="container">
        <div class="row">
            <div class="col-100">
                <ul class="list-unstyled d-flex justify-content-center">
                    <li v-for="img, index in clientsImg" :key="index">
                        <img :src="img.src" alt="">
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
            clientsImg: [
                {
                    nome: '',
                    src: '/public/img/h1-clients-img-4.png'
                },
                {
                    nome: '',
                    src: '/public/img/h1-clients-img-3.png'
                },
                {
                    nome: '',
                    src: '/public/img/h1-clients-img-1.png'
                },
                {
                    nome: '',
                    src: '/public/img/h1-clients-img-2.png'
                },
                {
                    nome: '',
                    src: '/public/img/h1-clients-img-5.png'
                }
            ]
        }
    }
}
</script>

<style scoped>
    .container {
        background-color: var(--bg-primary);
    }

    .col-100 {
        padding: 30px 0px;
    }

    li img {
        width: 100px;
        height: auto;
    }
</style>
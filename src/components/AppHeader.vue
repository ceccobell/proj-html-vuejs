<template>
    <header>
        <div class="navbar d-flex justify-content-between align-items-center">
            <!-- Sezione sinistra -->
            <div class="navbar-left">
                <button class="fs-12">ORDER ONLINE</button>
            </div>

            <!-- Sezione centrale -->
            <div class="navbar-center">
                <ul class="list-unstyled d-flex align-items-center">
                    <li v-for="(item, index) in navbarCenterItems" :key="index">
                        <a :href="item.href" v-if="item.type === 'link'" class="fs-10">
                            <img v-if="item.icon" :src="item.icon" class="icon" alt="icon" />
                            {{ item.text }}
                        </a>
                        <img v-if="item.type === 'image'" :src="item.src" :alt="item.alt" class="logo" />
                    </li>
                </ul>
            </div>

            <!-- Sezione destra -->
            <div class="navbar-right">
                <ul class="list-unstyled d-flex align-items-center">
                    <li v-for="item in navbarRightItems" :key="item.text">
                        <a :href="item.href" class="fs-10">
                            <img v-show="item.icon" :src="item.icon" class="icon" alt="icon" />
                            <i v-show="item.text == 'SEARCH'" class="fa-solid fa-magnifying-glass"></i>
                            {{ item.text }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="container">
            <div class="row">
                <div class="col-25 d-flex align-items-center">
                    <div class="circle">
                        <button class="previous-btn fs-10"  @click="prevImage">PREV</button>
                    </div>
                </div>
                <div class="container-img">
                    <img :src="currentBgImage" alt="" class="bg-img">
                    <img :src="currentFeaturedImage" alt="" class="featured-img">
                </div>
                <div class="col-25 d-flex align-items-center justify-content-end">
                    <div class="circle">
                        <button class="next-btn fs-10" @click="nextImage">NEXT</button>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    props: {
        navbarCenterItems: Array,
        navbarRightItems: Array
    },
    data() {
        return {
            currentImageIndex: 0,
            images: [
                {
                    bg: '/public/img/h3-rev-img-5.png',
                    featured: '/public/img/h3-rev-img-6.png'
                },
                {
                    bg: '/public/img/h3-rev-img-1.png',
                    featured: '/public/img/h3-rev-img-2.png'
                },
                {
                    bg: '/public/img/h3-rev-img-3.png',
                    featured: '/public/img/h3-rev-img-4.png'
                }
            ]
        };
    },
    computed: {
        currentBgImage() {
            return this.images[this.currentImageIndex].bg;
        },
        currentFeaturedImage() {
            return this.images[this.currentImageIndex].featured;
        }
    },
    methods: {
        nextImage() {
            this.currentImageIndex = (this.currentImageIndex + 1) % this.images.length;
        },
        prevImage() {
            this.currentImageIndex =
                (this.currentImageIndex - 1 + this.images.length) % this.images.length;
        }
    }
}
</script>

<style scoped>
    header {
        background-image: url(../../public/img/cielostellato.PNG);
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        padding: 20px 0px;
    }

    .navbar {
        width: 80%;
        margin: 0 auto;
    }

    .navbar button {
        color: var(--text-secondary);
        background-color: var(--bg-button);
        border: 0;
        padding: 10px 20px;
    }

    .logo {
        width: 100px;
        height: auto;
    }

    .icon {
        width: 15px;
        height: auto;
        filter: invert(1);
    }

    li {
        margin: 0px 10px;
    }

    a {
        color: var(--text-secondary);
        text-decoration: none;
    }
</style>

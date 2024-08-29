<template>
    <header>
        <div class="navbar d-flex justify-content-between">
            <!-- Sezione sinistra -->
            <div class="navbar-left">
                <button>ORDER ONLINE</button>
            </div>

            <!-- Sezione centrale -->
            <div class="navbar-center">
                <ul class="list-unstyled d-flex">
                    <li v-for="(item, index) in navbarCenterItems" :key="index">
                        <a :href="item.href" v-if="item.type === 'link'">
                            <img v-if="item.icon" :src="item.icon" class="icon" alt="icon" />
                            {{ item.text }}
                        </a>
                        <img v-if="item.type === 'image'" :src="item.src" :alt="item.alt" />
                    </li>
                </ul>
            </div>

            <!-- Sezione destra -->
            <div class="navbar-right">
                <ul class="list-unstyled d-flex">
                    <li v-for="item in navbarRightItems" :key="item.text">
                        <a :href="item.href">
                            <img v-if="item.icon" :src="item.icon" class="icon" alt="icon" />
                            {{ item.text }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    props: {
        navbarCenterItems: Array,
        navbarRightItems: Array
    }
}
</script>

<style scoped>
    header {
        background-image: url(../../public/img/cielostellato.PNG);
    }
</style>

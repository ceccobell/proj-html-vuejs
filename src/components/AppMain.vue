<template>
    <AdvertisingSection :images="AdvertisingImgs" />
</template>

<script>
import AdvertisingSection from './AdvertisingSection.vue';

export default {
    components: {
        AdvertisingSection
    },
    data() {
        return {
            AdvertisingImgs: [
                {
                    src: '/public/img/h3-img-1.jpg',
                    clicked: false
                },
                {
                    src: '/public/img/h3-img-2.jpg',
                    clicked: false
                },
                {
                    src: '/public/img/h3-img-3.jpg',
                    clicked: false
                },
                {
                    src: '/public/img/h3-img-4.jpg',
                    clicked: false
                },
            ]
        }
    }
}
</script>

<style scoped>
    
</style>
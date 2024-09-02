<template>
    <div class="container">
        <div class="row">
            <div class="footer-left bg-cielostellato">
                <div class="col-33">
                    <h3 class="text-tertiary fs-12">FIND OUR RESTAURANTS</h3>
                    <ul class="list-unstyled">
                        <li v-for="restaurant, index in ourRestaurants" :key="index">
                            <div class="text-warning fs-10">{{ restaurant.via }}</div>
                            <div class="text-warning fs-10">{{ restaurant.city }}</div>
                            <div class="text-warning fs-10">{{ restaurant.telefono }}</div>
                        </li>
                    </ul>
                </div>
                <div class="col-33">
                    <h3 class="text-tertiary fs-12">WORKING HOURS</h3>
                    <ul class="list-unstyled">
                        <li v-for="hour, index in workingHours" :key="index">
                            <div class="text-tertiary fs-10">{{ hour.day }}</div>
                            <div class="fs-10" :class="hour.openingHours == 'Kitchen Closed' ? 'text-more-danger' : 'text-warning'">{{ hour.openingHours }}</div>
                        </li>
                    </ul>
                    <div class="text-tertiary fs-10 social">FOLLOW US:
                        <i v-for="(icon, index) in socialIcons" :key="index" :class="`fa-brands ${icon} text-white fs-8`"></i>
                    </div>
                </div>
                <div class="col-33">
                    <h1 class="text-white fs-12">THE DON PEPPE CREW FIRST AND FOREMOST VALUES AN AUTHENTIC, WELL BAKED SLICE OF PIZZA.</h1>
                </div>
                <div class="col-100 d-flex justify-content-between align-items-end">
                    <div class="fs-8 text-tertiary">Created with &hearts; by <span class="text-success">Qode Interactive</span></div>
                    <img src="/public/img/footer-bottom-img.png" alt="">
                </div>
            </div>
            <div class="footer-rigth"></div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        ourRestaurants: Array,
        workingHours: Array
    },
    data() {
        return {
            socialIcons: [
                'fa-twitter',
                'fa-facebook-f',
                'fa-square-instagram',
                'fa-linkedin-in'
            ]
        }
    }
}
</script>

<style scoped>
    .footer-left, .footer-rigth {
        width: 50%;
        padding: 50px 20px 30px 20px;
    }

    .footer-left {
        display: flex;
        flex-wrap: wrap;
    }

    .footer-rigth {
        background-image: url(/public/img/footer-img-1.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
    }

    li {
        margin: 10px 0px;
    }

    .social {
        margin-top: 30px;
    }

    i {
        margin: 0px 5px;
    }

    img {
        width: 70px;
        height: auto;
    }
</style>
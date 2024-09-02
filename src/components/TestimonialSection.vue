<template>
    <div class="container">
        <div class="row">
            <div class="col-25 d-flex align-items-center">
                <div class="circle">
                    <button class="previous-btn fs-10" @click="prevTestimonial">PREV</button>
                </div>
            </div>
            <div class="col-50 text-center">
                <h1 class="text-tertiary">"</h1>
                <h2 class="fs-18">"{{ currentTestimonial.text }}"</h2>
                <span class="fs-10 text-danger">{{ currentTestimonial.source }}</span>
                <div class="d-flex justify-content-center">
                    <span
                        v-for="(testimonial, index) in testimonials"
                        :key="index"
                        :class="['circle-sm', { 'bg-testimonial': index !== currentTestimonialIndex, 'text-tertiary': index === currentTestimonialIndex }]"
                    ></span>
                </div>
            </div>
            <div class="col-25 d-flex align-items-center justify-content-end position-relative">
                <div class="circle">
                    <button class="next-btn fs-10" @click="nextTestimonial">NEXT</button>
                </div>
                <div class="icon-pizza">
                    <img src="/public/svg/svg-4.svg" alt="" class="icon-pizza-img">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            currentTestimonialIndex: 0,
            testimonials: [
                {
                    text: "FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES",
                    source: "WASHINGTON POST 2018"
                },
                {
                    text: "THE PIZZA HERE IS BETTER THAN IN ANY PIZZERIA IN NEW YORK, A TRUE HIDDEN GEM!",
                    source: "NEW YORK TIMES 2019"
                },
                {
                    text: "IF YOU HAVEN'T TRIED THEIR PIZZA YET, YOU'RE MISSING OUT ON SOMETHING TRULY SPECIAL.",
                    source: "FOOD BLOGGER 2020"
                }
            ]
        };
    },
    mounted() {
        this.startAutoSlide();
    },
    computed: {
        currentTestimonial() {
            return this.testimonials[this.currentTestimonialIndex];
        }
    },
    methods: {
        nextTestimonial() {
            this.currentTestimonialIndex = (this.currentTestimonialIndex + 1) % this.testimonials.length;
        },
        prevTestimonial() {
            this.currentTestimonialIndex = (this.currentTestimonialIndex - 1 + this.testimonials.length) % this.testimonials.length;
        },
        startAutoSlide() {
            this.interval = setInterval(this.nextTestimonial, 5000);
        }
    }
};
</script>

<style scoped>
    .container {
        background-image: url(../../public/img/h3-testimonials-bckgrnd.jpg);
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }

    .col-50 {
        padding: 50px 0px;
    }

    .circle-sm {
        margin: 10px 3px;
        width: 5px;
        height: 5px;
        border-radius: 50%;
    }

    .circle-sm.bg-testimonial {
        background-color: var(--bg-testimonial);
    }

    .circle-sm.text-tertiary {
        background-color: var(--text-tertiary);
    }
</style>

<template>
    <div class="container">
        <div class="row">
            <div class="col-25 d-flex align-items-center">
                <div class="circle">
                    <button class="previous-btn fs-10">PREV</button>
                </div>
            </div>
            <div class="col-50 text-center">
                <h1 class="text-tertiary">"</h1>
                <h2 class="fs-18">"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES"</h2>
                <span class="fs-10 text-danger">WASHINGTON POST 2018</span>
                <div class="d-flex justify-content-center">
                    <span class="circle-sm text-tertiary"></span>
                    <span class="circle-sm bg-testimonial"></span>
                    <span class="circle-sm bg-testimonial"></span>
                </div>
            </div>
            <div class="col-25 d-flex align-items-center justify-content-end position-relative">
                <div class="circle">
                    <button class="next-btn fs-10">NEXT</button>
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
    
}
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

    .circle-sm:nth-child(1) {
        background-color: var(--text-tertiary);
    }

    .circle-sm:nth-child(2),
    .circle-sm:nth-child(3) {
        background-color: var(--bg-testimonial);
    }
</style>
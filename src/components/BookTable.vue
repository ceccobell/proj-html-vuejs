<template>
    <div class="container">
        <div class="row">
            <div class="col-100 d-flex justify-content-center">
                <div class="form-container">
                    <div class="input-group">
                        <input type="text" placeholder="1 Person">
                        <span class="icon"><img src="/public/svg/people-svgrepo-com.svg" alt="Icon"></span>
                    </div>
                    <span class="text-white fs-10">FOR</span>
                    <div class="input-group">
                        <input type="text" placeholder="11/29/2020">
                        <span class="icon"><img src="/public/svg/calendar-svgrepo-com.svg" alt="Icon"></span>
                    </div>
                    <span class="text-white fs-10">AT</span>
                    <div class="input-group">
                        <input type="text" placeholder="7:00 pm">
                        <span class="icon"><img src="/public/svg/clock-svgrepo-com.svg" alt="Icon"></span>
                    </div>
                    <button class="text-white">BOOK A TABLE</button>
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
        margin: 5px 0px;
    }

    .col-100 {
        background-image: url(/public/img/h3-background-img-3.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
        padding: 40px 0px;
    }

    .form-container {
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .input-group {
        position: relative;
    }

    input[type="text"] {
        padding-right: 30px;
        padding-left: 10px;
        width: 160px;
        height: 40px;
        font-size: 12px;
        border: 1px solid black;
    }

    .icon {
        position: absolute;
        top: 50%;
        right: 10px;
        transform: translateY(-50%);
    }

    .icon img {
        width: 20px;
        height: 20px;
    }

    button {
        background-color: var(--bg-button);
        border: 0;
        width: 200px;
        height: 40px;
    }
</style>
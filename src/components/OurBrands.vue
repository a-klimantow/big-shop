<template>
    <section class="brand container">
        <div class="brand__contant">
            <h2 class="main-title brand__title">Our Brands</h2>
            <p class="main-subtitle">
                Small Shoes 2017 new Arrival mini Messenger <span>Classic Shoes</span>
            </p>
            <p class="main__text">
                In porttitor elit ac mi placerat hendrerit. Morbi accumsan, erat in ullamcorper consectetur, nisi erat efficitur eros, sagittis tristique odio turpis vitae dui. Vestibulum gravida est ut erat pretium, non pretium diam feugiat. Integer egestas suscipit lorem ac fermentum. Integer at mauris vitae justo sagittis dapibus. Pellentesque sit amet visl vitae orci vehicula faucibus. Fusce et lat, feugiat eat.
            </p>
        </div>
        <div class="brand__image">
            <img src="../assets/img/iphone.png" alt="iphone" width="320px">
        </div>
    </section>
</template>

<script>
export default {
    
}
</script>

<style>
    .brand {
        padding: 120px 15px;
        display: grid;
        grid-template-columns: 1fr 1fr;
        align-items: center;
    }

    .brand__title {
        margin-bottom: 30px;
    }

    .brand__image {
        justify-self: center;
        position: relative;
    }

    .brand__image img {
        position: relative;
        z-index: 10;
    }

    .brand__image::before, .brand__image::after {
        content: '';
        display: block;
        border-radius: 50%;
        background-position: 50% 50%;
        position: absolute;
        top: 0%;
        left: 50%;
        transform: translate(-30%, -20%);
    }

    .brand__image::before {
        box-shadow: 0px 5px 47.5px 2.5px rgba(220, 220, 220,.75);
        background-image: url('../assets/img/shape-1.jpg');
        width: 390px;
        height: 390px;
    }

    .brand__image::after {
        background-color: #fff;
        width: 300px;
        height: 300px;
        top: 4%;
        left: 55%;
    }

    

    .main-subtitle {
        font-size: 25px;
    }

    .main-subtitle span {
        color: #8d83f9;
    }

    .main__text {
        color: #888;
        font-size: 16px;
        line-height: 26px;
        padding-right: 40px;
    }
</style>

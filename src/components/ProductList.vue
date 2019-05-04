<template>
    <section class="products">
        <div class="container">
            <h2 class="products__title main-title">Trendy Arrivals</h2>
            <ul class="products__list">
                <li class="products__item"
                    v-for="item in 6" :key="item">
                    <div class="products__item_top">
                        <div>
                            <i class="far fa-heart"></i>
                            253
                        </div>
                        <div>
                            <i class="far fa-comment-alt"></i>
                            120
                        </div>
                    </div>
                    <figure>
                        <img src="../assets/img/bag-1.jpg" alt="item">
                        <figcaption>
                            <h3 class="products__item-title">
                                Black Genuine Leather Bags
                                <span class="products__price">&#36; 25.20</span>
                            </h3>
                        </figcaption>
                    </figure>
                    <button class="products__button">Add to Cart</button>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    
}
</script>

<style>
    .products {
        max-width: 1385px;
        margin: 0 auto;
        position: relative;
        background-color: #fff;
        z-index: 10;
        box-shadow: 0 5px 47.5px 2.5px rgba(237, 235, 253, 0.75);
        padding-top: 90px;
        text-align: center;

    }

    .products__title {
        margin-bottom: 90px;
    }

    .products__list {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-gap: 30px;
    }

    .products__item {
        padding: 20px;
        position: relative;
        transition: box-shadow .5s ease;
    }

    .products__item_top {
        display: flex;
        justify-content: space-between;
        color: #bbb;
        font-size: 14px;
        margin-bottom: 20px;
        opacity: 0;
        transition: opacity .5s ease;
    }

    .products__item_top div {
        cursor: pointer;
    }

    .fa-heart {
        color: #f95889;
    }

    .fa-comment-alt {
        color: #72dcec;
    }

    .products__item-title {
        color: #777;
        font-size: 18px;
        font-weight: 400;
        margin-bottom: 50px;
        transition: color .5s ease;
    }

    .products__price {
        display: block;
        color: #333;
        font-size: 25px;
        font-weight: 600;
        margin-top: 18px;
        transition: color .5s ease;
    }

    .products__button {
        background-image: linear-gradient(64deg, rgb(140, 132, 249) 0%, rgb(161, 101, 244) 100%);
        color: #fff;
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translate(-50%, 50%);
        cursor: pointer;
        opacity: 0;
        transition: opacity .5s ease;
    }

    .products__item:hover {
        box-shadow: 0 5px 47.5px 2.5px rgba(237, 235, 253, 0.75);
    }

    .products__item:hover .products__item-title {
        color: #333;
    }

    .products__item:hover .products__price {
        color: #8c84f9;
    }

    .products__item:hover .products__item_top {
        opacity: 1;
    }

    .products__item:hover .products__button {
        opacity: 1;
    }


</style>

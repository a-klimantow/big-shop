<template>
    <section class="products">
        <div class="container">
            <h2 class="products__title main-title">Trendy Arrivals</h2>
            <ul class="products-menu"
                v-if="showMenu">
                <li v-for="(item, index) in menu" 
                    :key="item.title">
                    <a href="#" class="products-menu__link"
                        :class="{ 'products-menu__link_active': item.isActive }"
                        @click.prevent="chengeActive(index)">
                        {{ item.title }}
                    </a>
                </li>

            </ul>
            <ul class="products__list">
                <li class="products__item"
                    v-for="(item, index) in products" :key="index">
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
                        <img :src='"../assets/img/" + item.image + ".jpg"' :alt="item.image">
                        <figcaption>
                            <h3 class="products__item-title">
                                {{ item.title }}
                                <span class="products__price">&#36; {{ item.price.toFixed(2) }}</span>
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
    props: {
        showMenu: Boolean,
        products: Array
    },
    data() {
        return {
            menu: [
                {
                    title: "Fashion",
                    isActive: false
                },
                {
                    title: "Furnitures",
                    isActive: false
                },
                {
                    title: "Watches",
                    isActive: true
                },
                {
                    title: "Mobile",
                    isActive: false
                },
                {
                    title: "Cloth",
                    isActive: false
                },
                {
                    title: "Toys",
                    isActive: false
                }
            ]
        }
    },
    methods: {
        chengeActive(index) {
            this.menu.map((el) => el.isActive = false);
            this.menu[index].isActive = true;
        }
    }
    
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
        padding-bottom: 140px;
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
        min-height: 450px;
        display: flex;
        flex-direction: column;
    }

    .products__item_top {
        display: flex;
        justify-content: space-between;
        color: #bbb;
        font-size: 14px;
        margin-bottom: auto;
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

    .products-menu {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        width: 1105px;
        border-radius: 50px;
        min-height: 66px;
        box-shadow: 0px 5px 47.5px 2.5px rgba(239, 239, 240, .75);
        margin-bottom: 50px;
        font-size: 15px;

    }

    .products-menu li {
        width: 100px;
        text-align: center;
    }

    .products-menu__link:hover {
        color: rgb(179, 148, 250);
    }

    .products-menu__link_active{
        font-size: 20px;
        color: rgb(179, 148, 250);
        text-shadow: 0px 9px 5px rgba(213, 200, 247, .75);
    }
</style>

<template>
    <div id="app">
        <app-header></app-header>
        <main>
            <product-list class="trendy" :products="bags"></product-list>
            <brands></brands>
            <product-list class="showcase" :showMenu="true" :products="watch"></product-list>
            <newsletter></newsletter>
        </main>
        <app-footer></app-footer>
    </div>
</template>

<script>
    import Header from './components/Header/Header.vue';
    import ProductList from './components/ProductList.vue';
    import Brands from './components/OurBrands.vue';
    import Newsletter from './components/Newsletter.vue';
    import { bags } from './assets/bags.js';
    import { watch } from './assets/watch.js';
    import Footer from './components/Footer.vue';

    export default {
        name: 'app',
        components: {
        appHeader: Header,
        ProductList,
        Brands,
        Newsletter,
        appFooter: Footer
        },
        data() {
            return {
                bags: bags,
                watch: watch
            }
        }
    }
</script>

<style>
    body {
        padding: 0;
        margin: 0;
        font-family: 'Open Sans', sans-serif;
        font-size: 18px;
    }

    * {
        box-sizing: border-box;
    }

    ul, li {
        margin: 0;
        padding: 0;
        list-style: none;
    }

    figure {
        margin: 0;
        padding: 0;
    }

    button {
        border:none;
        font-size: 20px;
        box-shadow: 0 5px 23.57px 1.25px rgba(189, 227, 239, 0.75);
        border-radius: 30px;
        width: 202px;
        height: 60px;
    }

    a {
        color: inherit;
        text-decoration: none;
        outline: none;
    }

    #app {
        max-width: 1600px;
        margin: 0 auto;
        overflow: hidden;
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding-left: 15px;
        padding-right: 15px;
    }

    .main-title {
        font-size: 50px;
        color: #333;
        margin-top: 0;
    }

    .trendy {
        margin-top: -40px;
    }

    .showcase {
        margin-bottom: -40px;
        z-index: 10;
    }

</style>

<template>
    <header class="header">
        <div class="container">
            <div class="header__top">
                <logo></logo>
                <header-menu></header-menu>
            </div>
            <div class="header__center">
                <div class="header__content">
                    <h1 class="header__title">
                        <span>Summer</span><br/>
                        Collection
                    </h1>
                    <p class="header__subtitle"><span>25%</span> off</p>
                        <button class="header__button">
                            Details
                            <i class="fas fa-long-arrow-alt-right"></i>
                        </button>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
import Logo from '../Logo.vue';
import HeaderMenu from './HeaderMenu.vue';

export default {
    name: 'Header',
    components: {
        Logo,
        HeaderMenu
    },
    props: {
        msg: String
    } 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
    .header {
        min-height: 100vh;
        background-image: url('../../assets/img/main-bg.jpg');
        background-repeat: no-repeat;
        background-size: auto 92%;
        background-position: bottom left;
        position: relative;
        padding-top: 80px;
        color: #fff;
    }

    .header::before {
        content: '';
        display: block;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        clip-path: polygon(0 0, 100% 0, 100% 100%, 0 30%);
        background: 
        url('../../assets/img/pattern-main-bg.png') no-repeat,
        linear-gradient(63deg,#1100ff, #aa55f3);
        opacity: .5;
    }

    .header__top, .header__content {
        z-index: 10;
        position: relative;

    }

    .header__top {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 200px;
    }

    .header__center {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
    }


    .header__title, .header__subtitle {
        font-family: 'Roboto', sans-serif;
    }

    .header__title {
        font-size: 115px;
        line-height: 120px;
        margin-bottom: 10px;
    }

    .header__title span {
        color: #090000;
    }

    .header__subtitle {
        font-size: 50px;
        font-weight: 500;
        margin-top: 0;
        text-transform: uppercase;
        margin-bottom: 95px;
    }

    .header__subtitle span {
        color: #fbf934;
    }

    .header__button {
        background-color: rgb(252, 252, 252);
        color: #151515;
    }

    .fa-long-arrow-alt-right {
        color: #7048e2;
        margin-left: 17px;
    }

</style>

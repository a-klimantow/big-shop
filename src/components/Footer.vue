<template>
    <footer class="footer">
        <div class="container">
            <h2 class=footer__title>Big Shop</h2>
            <ul class="footer__list">
                <li class="footer__item"
                    v-for="item in menu"
                    :key=item>
                    <a href="#" class="footer__link">
                        {{ item }}
                    </a>
                </li>
            </ul>

            <ul class="social">
                <li class="social__item"
                    v-for="item in social"
                    :key="item.title">
                    <a href="#" class="social__link">
                        <i class="fab"
                            :class="item.icon"></i>
                        {{ item.title }}
                    </a>
                </li>
            </ul>
        </div>
        <div class="footer__copyright">
            &copy; Copyright 2017. Big Shop by Victor Themes
        </div>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            menu: ['Man', 'Woman', 'Kids', 'Bags', 'Watches', 'Toys'],
            social: [
                {
                    title: 'facebook',
                    icon: 'fa-facebook-f',
                    href: 'https://facebook.com'
                },
                {
                    title: 'google',
                    icon: 'fa-google-plus-g',
                    href: 'https://google.com'
                },
                {
                    title: 'instagram',
                    icon: 'fa-instagram',
                    href: 'https://instagram.com'
                },
                {
                    title: 'twitter',
                    icon: 'fa-twitter',
                    href: 'https://twitter.com'
                }
            ]
        }
    }
}
</script>

<style>
    .footer {
        text-align: center;
        padding-top: 75px;
    }

    .footer__title {
        color: #222;
        font-family: 'Roboto', sans-serif;
        font-weight: 500;
        font-size: 40px;
        margin-top: 0;
        margin-bottom: 45px;
    }

    .footer__list, .social {
        display: flex;
        justify-content: space-between;
        margin: 0 auto;
        margin-bottom: 50px;

    }

    .footer__list {
        max-width: 530px;
        color: #404040;
        font-weight: 600;
    }

    .social {
        max-width: 310px;
        color: #555;
    }

    .social__link {
        display: inline-flex;
        width: 56px;
        height: 56px;
        border-radius: 50%;
        font-size: 0px;
        border: 2px solid #ecebed;
        justify-content: center;
        align-items: center;
        transition: all .5s ease;
    }

    .social__link .fab {
        font-size: 25px;
    }

    .social__link:hover {
        background-image: linear-gradient(63deg, rgb(140, 132, 239) 0%, rgb(155, 109, 245) 99%);
        box-shadow: 0px 8px 19px 1px rgba(207, 207, 208, .75);
        color: #fff;
    }

    .footer__copyright {
        min-height: 65px;
        background-color: #f6f5f7;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 15px;
        color: #777;
    }
</style>

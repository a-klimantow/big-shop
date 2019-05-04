<template>
    <section class="newsletter">
        <h2 class="newsletter__title">Newsletter</h2>
        <form action="" class="form">
            <input type="text" class="form__input" placeholder="Enter your email address...">
            <button type="submit" class="form__button">Submit</button>
        </form>
    </section>
</template>

<script>
export default {
    
}
</script>

<style>
    .newsletter {
        min-height: 492px;
        text-align: center;
        background-image: linear-gradient(45deg, rgb(140, 132, 249) 0%, rgb(161, 101, 244) 100%);
        display: flex;
        flex-direction: column;
        align-items: center;
        position: relative;
    }

    .newsletter__title::before {
        content: 'get notified';
        position: absolute;
        font-size: 150px;
        font-family: 'Roboto', sans-serif;
        font-weight: bolder;
        text-transform: uppercase;
        width: 100%;
        left: 50%;
        top: 35%;
        transform: translate(-50%, -50%);
        opacity: .04;

        
    }

    .newsletter__title {
        margin-top: auto;
        font-size: 50px;
        color: #fff;
        margin-bottom: 80px;
    }

    .form {
        margin-bottom: auto;
        width: 850px;
        display: flex;
        padding: 5px;
        background-color: #fff;
        border-radius: 50px;
    }

    .form__input {
        flex-grow: 1;
        border-radius: inherit;
        border: none;
        padding-left: 28px;
        font-size: 20px;
    }

    .form__button {
        background-image: linear-gradient(45deg, rgb(140, 132, 249) 0%, rgb(161, 101, 244) 100%);
        color: #fff;
    }
</style>

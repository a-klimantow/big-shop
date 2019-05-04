<template>
    <div id="app">
        <app-header></app-header>
    </div>
</template>

<script>
    import Header from './components/Header.vue'

    export default {
        name: 'app',
        components: {
        appHeader: Header
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

    .title {
        font-family: 'Roboto', sans-serif;
    }
</style>

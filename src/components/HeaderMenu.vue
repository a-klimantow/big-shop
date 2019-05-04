<template>
    <div class="header__menu">
        <div class="header__search">
            <i class="fas fa-search"></i>
            Search
        </div>
        <div class="header__collection">
            Collection
            <i class="fas fa-chevron-down"></i>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
    .header__menu {
        font-weight: 600;
        min-width: 371px;
        height: 65px;
        background-color: #fff;
        display: flex;
        text-align: center;
        align-items: center;
        border-radius: 30px;
        color: #151515;
        box-shadow: 0 5px 23.57px 1.25px rgba(189, 227, 239, 0.75);
    }

    .header__search, .header__collection {
        width: 50%;
    }

    .header__search {
        border-right: 1px solid #6c6c6c;
    }

    .fa-search {
        margin-right: 17px;
    }

    .fa-chevron-down {
        margin-left: 17px;
    }


</style>

<template>
    <nav>
        <nuxt-link to="/">
            <img src="@/assets/images/logo.png" class="logo" alt="logo">
        </nuxt-link>
        <div class="menu">
            <nuxt-link to="/" class="ref">Главная</nuxt-link>
            <nuxt-link to="/about" class="ref">О нас</nuxt-link>
            <nuxt-link to="/form" class="ref">Запись</nuxt-link>
        </div>
    </nav>
</template>
<style scoped>
    nav{
        padding: 50px 100px;
    }
    .ref{
        color: #000;
        margin-right: 30px;
        font-family: "Roboto";
    }
    .logo{
        background-color:rgb(255, 231, 235);
        width: 100px;
        height: 100px;
        vertical-align: bottom;
        margin-top: -30px;
    }
    .menu{
        display: flex;
        justify-content: right;
        margin-top: -70px;
    }
</style>
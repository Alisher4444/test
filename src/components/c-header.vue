<template>
<div class="header">
    <div class="logo">
        <img src="../assets/Logo.svg" alt="">
    </div>

    <div class="links" v-show="humburger">
        <ul>
            <li>
                <a href="#">Главная</a>
            </li>
            <li>
                <a href="#">Наши преимущества</a>
            </li>
            <li>
                <a href="#">История Exline</a>
            </li>
            <li>
                <a href="#">Нам доверяют</a>
            </li>
            <li>
                <a href="#">Контакты</a>
            </li>
        </ul>
        <ul class="call_to_action">
            <li>
                <a href="#">info@exline.kz</a>
            </li>
            <li>
                <a href="#">+7 (777) 707 87 77</a>
            </li>
        </ul>
    </div>
    <div class="humburger" @click="$emit('showBurger')">
        Бургер
    </div>
</div>
</template>

<script>
export default {
    name: 'App',
    props: {
        humburger: Boolean
    },

}
</script>

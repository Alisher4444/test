<template>
    <div class="app">
    
        <Header @showBurger="showBurger" :humburger="humburger"></Header>
    
        <div class="background">
            <div class="slider">
                <img src="../assets/images/Banner.jpg" alt="">
            </div>
    
        </div>
    
        <Filter />
    
        <div class="advantages">
            <h1>Наши преимущества</h1>
            <div class="advantages-content">
                <div class="item">
                    <img src="../assets/fast-delivery-2.svg" alt="">
                    <p>Быстрая доставка</p>
                </div>
                <div class="item">
                    <img src="../assets/fast-delivery-4.svg" alt="">
                    <p>Доставим в любую точку города и области</p>
                </div>
                <div class="item">
                    <img src="../assets/fast-delivery-1.svg" alt="">
                    <p>Ежедневные отправки</p>
                </div>
                <div class="item">
                    <img src="../assets/fast-delivery-3.svg" alt="">
                    <p>Собственный склад</p>
                </div>
            </div>
    
        </div>
    
        <div class="history">
            <h1>История Exline</h1>
            <div class="history-content">
                <div class="item">
                    <div class="item-txt">
                        <p class="item-txt-title">Курьерская компания Exline основана 31 июля 2003 года</p>
                        <p class="item-txt-full">За время работы компания Exline заняла достойную нишу на рынке почтовых услуг, зарекомендовав себя как надежного партнера, которому доверяют свои отправления многие компании казахстанского и международного бизнеса</p>
                    </div>
                    <img src="../assets/first.jpg" alt="">
                </div>
                <div class="item">
                    <img src="../assets/second.jpg" alt="">
                    <div class="item-txt">
                        <p class="item-txt-title">Курьерская компания Exline основана 31 июля 2003 года</p>
                        <p class="item-txt-full">За время работы компания Exline заняла достойную нишу на рынке почтовых услуг, зарекомендовав себя как надежного партнера, которому доверяют свои отправления многие компании казахстанского и международного бизнеса</p>
                    </div>
                </div>
            </div>
        </div>
    
        <div class="partners">
            <h1>Нам доверяют </h1>
            <div class="partners-content">
                <img src="../assets/techno.svg" alt="">
                <img src="../assets/kaspi.svg" alt="">
                <img src="../assets/astanamotors.svg" alt="">
                <img src="../assets/zepter.svg" alt="">
    
                <img src="../assets/gazprom.svg" alt="">
                <img src="../assets/philips.svg" alt="">
                <img src="../assets/kaztranscom.svg" alt="">
                <img src="../assets/microsoft.svg" alt="">
            </div>
        </div>


        <div class="contact">
            <h1>Контакты </h1>
            <div class="address">
                <p class="address_point">г. Алматы,  улица Жетысуская, 43</p>
                <a href="#">+7 (727) 390‒03‒00</a>
                <a href="#">+7 (727) 390‒03‒00</a>
                <a href="#">+7 (727) 390‒03‒00</a>
                <a href="#">+7 (727) 390‒03‒00</a>

                <a href="#">info@exline.kz</a>
            </div>
            <div id="map" style="width:100%; height:600px"></div>
        </div>
        
    
        <div class="footer">
            <div class="logo">
                <img src="../assets/Logo.svg" alt="">
            </div>
            <div class="media">
                <a href="#">
                    <img src="../assets/images/insta.svg" alt="">
                </a>
                <a href="#">
                    <img src="../assets/images/insta.svg" alt="">
                </a>
                <a href="#">
                    <img src="../assets/images/insta.svg" alt="">
                </a>
            </div>
            <div class="rules">
                <p>© Все права защищены 2023</p>
            </div>
        </div>
    
    </div>
</template>

<script>
import Header from '../components/c-header.vue'
import Filter from '../components/c-filter.vue'

export default {
    name: 'App',
    props: {
        msg: String
    },

    components: {
        Header,
        Filter
    },


    data() {
        return {    
            humburger: true,
        }
    },

    methods: {
        showBurger() {
            this.humburger = !this.humburger
        },

 
    }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

<template>
    <div class="app">
    
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
            <div class="humburger" @click.prevent="showBurger()">
                Бургер
            </div>
        </div>
    
        <div class="background">
    
    
        </div>
    
        <div class="filter">
            <div class="calc">
                <div class="calc-item">
                    <p>Рассчитать стоимость</p>
                </div>
                <div class="calc-item">
                    <p>Вызвать курьера</p>
                </div>
                <div class="calc-item">
                    <p>Отследить посылку</p>
                </div>
            </div>
            <div class="filter-content">
                <div class="form">
                    <div>
                        <input type="text" v-model="from" placeholder="Откуда">
                        <div class="tags">
                            <div class="tag" :class="{'active' : 'Астана' == from }" @click.prevent="tag('Астана', 'from')">
                                <p>Астана</p>
                            </div>
                            <div class="tag" :class="{'active' : 'Алматы' == from }" @click.prevent="tag('Алматы', 'from')">
                                <p>Алматы</p>
                            </div>
                            <div class="tag" :class="{'active' : 'Шымкент' == from }" @click.prevent="tag('Шымкент', 'from')">
                                <p>Шымкент</p>
                            </div>
                        </div>
                    </div>
                    <button class="switch" @click.prevent="swap()">
                      <img src="../assets/arrow-left-right.svg" alt="">
                    </button>
                    <div>
                        <input type="text" v-model="to" placeholder="Куда">
                        <div class="tags">
                            <div class="tag" :class="{'active' : 'Астана' == to }" @click.prevent="tag('Астана', 'to')">
                                <p>Астана</p>
                            </div>
                            <div class="tag" :class="{'active' : 'Алматы' == to }" @click.prevent="tag('Алматы', 'to')">
                                <p>Алматы</p>
                            </div>
                            <div class="tag" :class="{'active' : 'Шымкент' == to }" @click.prevent="tag('Шымкент', 'to')">
                                <p>Шымкент</p>
                            </div>
                        </div>
                    </div>
                    <button @click.prevent="getResult()" class="search">Рассчитать стоимость</button>
    
                </div>
                <div class="result">
                  <div class="result-item">
                    <img src="../assets/images/clock-icon.svg" alt="">
                    <p>Расстояние: <b>{{distance}} км</b></p>
                  </div>
                  <div class="result-item">
                    <img src="../assets/images/distance-icon.svg" alt="">
                    <p>Время: <b>{{time}} часа</b></p>
                  </div>
                  <div class="result-item">
                    <img src="../assets/images/tenge-icon.svg" alt="">
                    <p>Стоимость: <b>{{deliveryCost}} ₸</b></p>
                  </div>
                </div>
            </div>
    
        </div>
    
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
export default {
    name: 'App',
    props: {
        msg: String
    },


    data() {
        return {
            from: '',
            to: '',
            cities: [{
                    "id": 1,
                    "address": "Алматы"
                },
                {
                    "id": 2,
                    "address": "Астана"
                },
                {
                    "id": 3,
                    "address": "Кызылорда"
                },
                {
                    "id": 4,
                    "address": "Костанай"
                },
                {
                    "id": 5,
                    "address": "Петропавловск"
                },
                {
                    "id": 6,
                    "address": "Шымкент"
                }
            ],
            distances: [{
                    "from": 1,
                    "to": 2,
                    "value": 5551
                },
                {
                    "from": 1,
                    "to": 3,
                    "value": 1231
                },
                {
                    "from": 1,
                    "to": 4,
                    "value": 8585
                },
                {
                    "from": 1,
                    "to": 5,
                    "value": 8244
                },
                {
                    "from": 1,
                    "to": 6,
                    "value": 7554
                },
                {
                    "from": 2,
                    "to": 3,
                    "value": 5443
                },
                {
                    "from": 2,
                    "to": 4,
                    "value": 2299
                },
                {
                    "from": 2,
                    "to": 5,
                    "value": 4124
                },
                {
                    "from": 2,
                    "to": 6,
                    "value": 3210
                },
                {
                    "from": 3,
                    "to": 4,
                    "value": 8888
                },
                {
                    "from": 3,
                    "to": 5,
                    "value": 4411
                },
                {
                    "from": 3,
                    "to": 6,
                    "value": 4555
                },
                {
                    "from": 4,
                    "to": 5,
                    "value": 3211
                },
                {
                    "from": 4,
                    "to": 6,
                    "value": 8744
                },
                {
                    "from": 5,
                    "to": 6,
                    "value": 4553
                }
            ],
            distance: 0,
            humburger: false,
            time: 0,
            deliveryCost: 0,
        }
    },

    methods: {
        showBurger() {
            this.humburger = !this.humburger
        },

        swap() {
            let temp = this.to
            this.to = this.from
            this.from = temp
        },

        tag(city, type) {
            if (type == 'to') {
                this.to = city
            } else if (type == 'from') {
                this.from = city
            }
        },


        getResult() {
            let fromID = this.cities.find((item) => {
                return item.address == this.from
            })

            let toID = this.cities.find((item) => {
                return item.address == this.to
            })


            let distance = this.distances.find((item) => {
                if (item.from == fromID.id && item.to == toID.id) {
                    return item.value
                }
            })

            if (distance === 'undefined' || distance === undefined || distance === null) {
              this.distance = 0
            } else {
              this.distance = distance.value
            }

            


            if (this.distance < 100 && this.distance > 0) {
                this.time = 24
            } else if (this.distance > 100 && this.distance < 500) {
                this.time = 48
            } else if (this.distance >= 500) {
                this.time = 96
            } else if (this.distance == 0){
              this.distance = 0
              this.time = 0
              this.deliveryCost = 0
            }

            this.deliveryCost = this.distance * this.time
        }
    }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

<template>
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
</template>

<script>
export default {
    name: 'App',
    props: {
        msg: String,
    },

    data() {
        return {
            from: '',
            to: '',
            distance: 0,
            time: 0,
            deliveryCost: 0,
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
        }
    },

    methods: {
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
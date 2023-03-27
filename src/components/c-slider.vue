<template>
<div class="background">
    <button><img src="../assets/images/arrow.svg" alt=""></button>
    <div class="slider" v-for="item of sliders" v-bind:key="item.id">
        <img :src="item.src" v-if="item.visible" alt="">
    </div>
    <button @click.prevent="next()"><img src="../assets/images/arrow.svg" alt=""></button>

</div>
</template>

<script>
export default {
    name: 'App',

    data() {
        return {
            sliders: [
                {
                    id: 0,
                    src: require('../assets/images/Banner.jpg'),
                    alt: 'asdasd',
                    visible: true
                },
                {
                    id: 1,
                    src: 'https://media.sproutsocial.com/uploads/2017/02/10x-featured-social-media-image-size.png',
                    alt: 'asdasd',
                    visible: false
                },
                {
                    id: 2,
                    src: 'https://images.unsplash.com/photo-1575936123452-b67c3203c357?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8aW1hZ2V8ZW58MHx8MHx8&w=1000&q=80',
                    alt: 'asdasd',
                    visible: false
                }
            ],

            counter: 0
        }
    },


    methods: {
        next() {
            
        },

        prev () {

        }
    }

}
</script>

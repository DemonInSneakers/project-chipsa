<template>
    <Layout>
        <div class="swiper-container">
            <div class="swiper-wrapper">
                <div class="swiper-slide"><Page1 /></div>
                <div class="swiper-slide"><Page2 /></div>
                <div class="swiper-slide"><Page3 /></div>

            </div>
        </div>
    </Layout>
</template>

<script>
    import Swiper from 'swiper'
    import 'swiper/css/swiper.css'
    // import 'swiper/js/swiper.js'
    import Layout from '@/components/Layout';
    import Page1 from "@/components/Page1";
    import Page2 from "@/components/Page2";
    import Page3 from "@/components/Page3";

    export default {
        name: "Pages",
        components: {
            Page3,
            Page2,
            Page1,
            Layout
        },
        mounted () {
            this.initSwiper()
        },
        methods: {
            initSwiper () {
                const mySwiper = new Swiper('.swiper-container', {
                    direction: 'vertical',
                    slidesPerView: 1,
                    spaceBetween: 0,
                    mousewheel: true,
                })
                mySwiper.init()
            }
        }
    }


</script>

<style>
    .swiper-container {
        width: 100%;
        height: 100%;
        margin-left: auto;
        margin-right: auto;
    }
    .swiper-slide {
        overflow: hidden;
        color: #fff;
    }
</style>
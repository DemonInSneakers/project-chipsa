<template>
   <PageWrap>
       <div class="page-2">
           <div class="page-2__header">
               <h2>
                   Транспортные<br>
                   услуги
               </h2>
           </div>

           <div class="page-2__content">
               <div style="background-color: red;">
<!--                   <div class="page-2__swiper-container-1">-->
<!--                      <div class="swiper-wrapper">-->
<!--                          <div class="swiper-slide">Slide 1</div>-->
<!--                          <div class="swiper-slide">Slide 2</div>-->
<!--                      </div>-->
<!--                       <div class="swiper-pagination-1"></div>-->
<!--                  </div>-->
               </div>
               <div style="background-color: blue;">
                   <div class="page-2__swiper-container-2">
                       <div class="swiper-wrapper">
                           <div class="swiper-slide">Slide 1</div>
                           <div class="swiper-slide">Slide 2</div>
                       </div>
                       <div class="swiper-pagination-2"></div>
                   </div>
               </div>

           </div>



       </div>
   </PageWrap>
</template>

<script>
    import PageWrap from "@/components/PageWrap";
    import Swiper from 'swiper'
    import 'swiper/css/swiper.css'
    export default {
        name: "Page2",
        components: {PageWrap},
        data: function () {
            return {
                nameSlides: ['Основные', 'Дополнительные']
            }
        },
        mounted () {
            this.initSwiper()
        },
        methods: {
            initSwiper () {
                // var Swiper1 = new Swiper('.page-2__swiper-container-1', {
                //     pagination: {
                //         el: '.swiper-pagination-1',
                //         clickable: true,
                //         renderBullet: function (index, className) {
                //             return '<span class="' + className + '">' + (index + 1) + '</span>';
                //         },
                //     },
                // })
                // Swiper1.init()

                var Swiper2 = new Swiper('.page-2__swiper-container-2', {
                    pagination: {
                        el: '.swiper-pagination-2',
                        clickable: true,
                        // renderBullet: function (index, className) {
                        //     return '<span class="' + className + '">' + (index + 1) + '</span>';
                        // },
                    },
                })
                Swiper2.init()
            }
        }
    }
</script>

<style lang="sass" scoped>
    .page-2
        display: grid
        grid-template-rows: auto 1fr
        height: 100%
        margin: 0 -36px
        @media (max-width: 768px)
            margin: 0 -20px

        .page-2__header
            display: flex
            padding: 55px 36px 30px 36px
            background-color: #f2f5fa
            @media (max-width: 768px)
                padding: 20px
            h2
                font-size: 5vh
                color: #232930
                @media (max-width: 768px)
                    font-size: 4vh
        .page-2__content
            display: grid
            grid-template-columns: 1fr 1fr
            /*grid-template-rows: 1fr 1fr*/
            background-color: #e7ebf1

            .page-2__swiper-container-1
                width: 100%
                height: 100%
            .page-2__swiper-container-2
                width: 100%
                height: 100%



</style>
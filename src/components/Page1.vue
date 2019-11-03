<template>
   <PageWrap>
       <div class="page">
           <div class="left">
               <p class="title">
						<span>Из Китая в<br>
						Россию</span>
                   <br>
                   доставка<br>
                   любых грузов<br>
                   под ключ
               </p>

               <p class="descr">
                   от 45 кг до целого<br>
                   контейнера
               </p>

               <ButtonBasic ButtonType="white">Оставить заявку</ButtonBasic>

           </div>
           <div class="right">
               <p class="optional">
                   Компания PACIFIC ASIA GROUP с 2007 года предоставляет качественный сервис по доставке грузов из Китая.
               </p>
               <ButtonShift link="http://localhost:8080/" label="Смотреть видео" type="play"><IconPlay /></ButtonShift>
           </div>
       </div>
   </PageWrap>
</template>

<script>
    import PageWrap from "@/components/PageWrap";
    import ButtonBasic from "@/components/buttons/ButtonBasic";
    import ButtonShift from "@/components/buttons/ButtonShift";
    import IconPlay from "@/components/icons/IconPlay";
    export default {
        name: "Page1",
        components: {IconPlay, ButtonShift, ButtonBasic, PageWrap}
    }
</script>

<style lang="sass" scoped>
    .page
        display: flex
        width: 50%
        height: 100%
        padding: 55px 0
        @media (max-width: 1366px)
            width: 100%
        @media (max-width: 768px)
            padding: 20px 0
        .left
            display: flex
            justify-content: space-between
            flex-direction: column
            height: 100%
            .title
                line-height: 88%
                color: #f2f5fa
                /*@media (max-width: 1366px)*/
                /*    font-size: 3em*/
                /*@media (max-width: 1024px)*/
                /*    font-size: 2.5em*/
                @media (max-width: 768px)
                    font-size: 2.5em
                font-size: 7vh
                span
                    color: #616972
        .right
            display: flex
            flex-direction: column
            width: 260px
            margin-left: auto
            @media (max-width: 1366px)
                justify-content: flex-end
            .optional
                font-size: 1.1em
                color: #818992
                font-weight: 300
                line-height: 1.5
                margin-bottom: 20px
                @media (max-width: 768px)
                    line-height: 1.1


</style>
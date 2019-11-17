<template>
   <PageWrap>
       <div class="page">
           <h1 class="title">
                    <span>Из Китая в<br>
                    Россию</span>
               <br>
               доставка<br>
               любых грузов<br>
               под ключ
           </h1>

           <p class="optional">
               Компания PACIFIC ASIA GROUP с 2007 года предоставляет качественный сервис по доставке грузов из Китая.
           </p>

           <ButtonShift class="button-play" label="Смотреть видео"><IconPlay /></ButtonShift>

           <p class="descr">
               от 45 кг до целого<br>
               контейнера
           </p>

           <ButtonBasic class="button-request" type="white">Оставить заявку</ButtonBasic>

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
        display: grid
        grid-template-rows: auto auto 1fr auto
        grid-template-columns: 1fr 280px
        grid-gap: 3vh
        width: 50%
        height: 100%
        padding: 55px 0
        @media (max-width: 1366px)
            width: 100%
        @media (max-width: 768px)
            grid-template-columns: 1fr 1fr
            padding: 20px 0
        @media (max-height: 700px)
            padding: 20px 0

        .title
            grid-row-start: 1
            grid-column-start: 1
            grid-row-end: 3
            grid-column-end: 2
            font-size: 7vh
            color: #f2f5fa
            line-height: 88%
            @media (max-width: 768px)
                grid-column-end: 3
                font-size: 6vh


            span
                color: #616972

        .descr
            grid-row-start: 3
            grid-column-start: 1
            grid-row-end: 4
            grid-column-end: 2
            margin-bottom: auto
            font-size: 3vh
            color: #818992
            @media (max-width: 768px)
                font-size: 2.5vh

        .optional
            grid-row-start: 1
            grid-column-start: 2
            grid-row-end: 2
            grid-column-end: 3
            font-size: 1.1em
            color: #818992
            font-weight: 300
            line-height: 1.5
            @media (max-width: 1366px)
                grid-row-start: 1
                grid-row-end: 4
                margin-top: auto
            @media (max-width: 768px)
                display: none
            @media (max-height: 550px)
                font-size: 3vh

        .button-request
            grid-row-start: 4
            grid-column-start: 1
            grid-row-end: 5
            grid-column-end: 2

        .button-play
            grid-row-start: 2
            grid-column-start: 2
            grid-row-end: 3
            grid-column-end: 3
            margin-right: auto
            @media (max-width: 1366px)
                grid-row-start: 4
                grid-row-end: 5


</style>
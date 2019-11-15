<template>
    <header class="header">

        <div class="left">
            <ButtonShift label="Обратный звонок" link="tel:88005005493"><IconPhone /></ButtonShift>
        </div>

        <a href="/" class="logo"><IconLogo class="icon-logo" /></a>

        <div class="right">
            <Menu class="menu" v-if="$mq.desktop"/>
            <ButtonBasic class="button-inquiry" type="transparent">Запрос</ButtonBasic>
            <Hamburger />
        </div>
    </header>
</template>

<script>
    import IconLogo from "@/components/icons/IconLogo";
    import Menu from "@/components/Menu";
    import ButtonBasic from "@/components/buttons/ButtonBasic";
    import Hamburger from "@/components/buttons/Hamburger";
    import ButtonShift from "./buttons/ButtonShift";
    import IconPhone from "./icons/IconPhone";
    export default {
        name: "Header",
        components: {IconPhone, ButtonShift, Hamburger, ButtonBasic, Menu, IconLogo},
    }
</script>

<style lang="sass" scoped>
    .header
        display: flex
        flex: 0 0 auto
        width: 100%
        height: 122px
        padding: 0 36px
        box-sizing: border-box
        color: #94979E
        align-items: center
        justify-content: space-between
        @media (max-width: 1366px)
            height: 80px
        @media (max-width: 768px)
            height: 65px
            padding: 0 20px
        .left,
        .right
            display: flex
            width: 45%
            transition: transform .5s ease, opacity .5s ease
            align-items: center
            justify-content: space-between
        .menu
            margin-right: auto
        .button-inquiry
            margin-right: 30px
            @media (max-width: 1366px)
                margin-left: auto
            @media (max-width: 768px)
                margin-right: 20px
        .icon-logo
            @media (max-width: 768px)
                height: 30px

</style>
<template>
    <div>
        <div class="header">

            <div class="header__left">
                <ButtonPhone phone="88005005493" >8–800–500–54–93</ButtonPhone>
            </div>

            <a href="/" class="logo"><IconLogo class="iconLogo" /></a>

            <div class="header__right">
                <Menu v-if="$mq.desktop"/>
                <ButtonBasic class="header__button" ButtonType="transparent">Запрос</ButtonBasic>
                <Hamburger />
            </div>
        </div>
    </div>
</template>

<script>
    import IconLogo from "@/components/icons/IconLogo";
    import ButtonPhone from "@/components/buttons/ButtonPhone";
    import Menu from "@/components/Menu";
    import ButtonBasic from "@/components/buttons/ButtonBasic";
    import Hamburger from "@/components/buttons/Hamburger";
    export default {
        name: "Header",
        components: {Hamburger, ButtonBasic, Menu, ButtonPhone, IconLogo},
    }
</script>

<style lang="sass" scoped>
    .header
        display: flex
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
        .header__left,
        .header__right
            display: flex
            width: 45%
            transition: transform .5s ease, opacity .5s ease
            align-items: center
            justify-content: space-between
        .header__button
            margin-right: 30px
            margin-left: auto
            @media (max-width: 768px)
                margin-right: 20px
        .iconLogo
            @media (max-width: 768px)
                height: 30px

</style>
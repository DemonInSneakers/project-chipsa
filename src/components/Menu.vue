<template>
    <ul class="menu">
        <li class="menu__item"><a href="/price/">Стоимость</a></li>
        <li class="menu__item"><a href="/delivery/">Доставка из Китая</a></li>
        <li class="menu__item"><a href="/contacts/">Контакты</a></li>
    </ul>
</template>

<script>
    export default {
        name: "Menu"
    }
</script>

<style lang="sass" scoped>
    .menu
        font-family: 'Tinos'
        display: flex
        flex: 0 0 auto
        list-style: none
        transition: opacity .5s ease
        opacity: 1
        margin-right: auto
        margin-left: auto
        .menu__item
            margin-right: 30px
            a
                padding: 15px 0
                transition: opacity ease .5s
                text-decoration: none
                opacity: .5
                color: #FEFEFE
            a:hover
                opacity: 1

</style>
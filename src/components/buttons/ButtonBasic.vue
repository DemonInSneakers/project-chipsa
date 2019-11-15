<template>
    <button type="button" :class="'button-basic ' + type">
        <slot />
    </button>
</template>

<script>
    export default {
        name: "ButtonBasic",
        props: {
            type: String
        }
    }
</script>

<style lang="sass" scoped>
    .button-basic
        flex: 0 0 auto
        font-family: 'Tinos'
        font-size: .9em
        height: 40px
        width: auto
        padding: 0 30px 0 30px
        border-radius: 50px
        outline: none
        transition: background-color ease .4s
        @media (max-width: 768px)
            padding: 0 20px 0 20px
            height: 30px
            font-size: .8em

    .transparent
        color: #D1D7DB
        background-color: transparent
        border: 1px solid rgba(242, 245, 250, .3)
        @media (min-width: 768px)
            &:hover
                background-color: rgba(209, 215, 219, .3)
        @media (max-width: 768px)
            &:active
                background-color: rgba(209, 215, 219, .3)
    .white
        margin-right: auto
        color: #2D353F
        background-color: rgba(242, 245, 250, 1)
        border: 1px solid rgba(242, 245, 250, .3)
        @media (min-width: 768px)
            &:hover
                background-color: rgba(242, 245, 250, .7)
        @media (max-width: 768px)
            &:active
                background-color: rgba(242, 245, 250, .7)

</style>
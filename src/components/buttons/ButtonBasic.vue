<template>
    <div>
        <button type="button" :class="'button ' + ButtonType">
            <slot />
        </button>
    </div>
</template>

<script>
    export default {
        name: "ButtonBasic",
        props: {
            ButtonType: String
        }
    }
</script>

<style lang="sass" scoped>

    .button
        font-family: 'Tinos'
        font-size: .9em
        height: 40px
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
        &:hover
            background-color: rgba(209, 215, 219, .3)

    .white
        color: #2D353F
        background-color: #F2F5FA
        border: 1px solid rgba(242, 245, 250, .3)
        &:hover
            color: #D1D7DB
            background-color: transparent

</style>
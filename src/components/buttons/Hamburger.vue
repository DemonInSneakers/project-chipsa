<template>
    <a class="hamburger">
        <span></span>
        <span></span>
    </a>
</template>

<script>
    export default {
        name: "Hamburger"
    }
</script>

<style lang="sass" scoped>
    .hamburger
        outline: none
        position: relative
        display: block
        flex: 0 0 auto
        width: 40px
        height: 40px
        cursor: pointer
        transition: background-color ease .5s, border-color ease .5s
        background-color: rgba(242, 245, 250, 1)
        border: 1px solid rgba(151, 151, 151, 0)
        border-radius: 50%
        @media (min-width: 768px)
            &:hover
                background-color: rgba(242, 245, 250, .5)
        @media (max-width: 768px)
            width: 30px
            height: 30px
            &:active
                background-color: rgba(242, 245, 250, .5)
        span
            position: absolute
            top: 38%
            left: 25%
            display: block
            width: 50%
            height: 7%
            background-color: #2F3741
            &:last-child
                top: auto
                bottom: 38%

</style>
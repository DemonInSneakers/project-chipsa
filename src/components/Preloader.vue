<template>
    <div class="preloader">
        <div class="line"></div>
    </div>
</template>

<script>
    export default {
        name: "Preloader"
    }
</script>

<style lang="sass" scoped>
    .preloader
        padding: 0 36px
        @media (max-width: 768px)
            padding: 0 20px
        .line
            width: 100%
            height: 1px
            position: relative
            background-color: #fefefe
            transition: opacity .5s ease
            opacity: 1
</style>
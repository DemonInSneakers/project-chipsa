<template>
    <div class="page-wrap">
        <slot />
    </div>
</template>

<script>
    export default {
        name: "PageWrap"
    }
</script>

<style lang="sass" scoped>
    .page-wrap
        box-sizing: border-box
        width: 100%
        height: 100%
        padding: 0 36px
        @media (max-width: 768px)
            padding: 0 20px

</style>
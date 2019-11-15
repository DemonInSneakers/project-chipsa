<template>
    <footer class="footer">
        <p class="scroll-down" id="downScrollText">Листайте вниз</p>
        <p class="down-arrow" id="downScrollArrow" style="transform: rotate(0deg);"></p>
        <div class="social" v-if="$mq.phone">
            <a :href="LinkFacebook"><IconFacebook /></a>
            <a :href="LinkTwitter"><IconTwitter /></a>
        </div>
    </footer>
</template>

<script>
    import IconTwitter from "@/components/icons/IconTwitter";
    import IconFacebook from "@/components/icons/IconFacebook";
    export default {
        name: "footer",
        components: {IconFacebook, IconTwitter},
        data: function () {
            return {
                LinkFacebook: "https://www.facebook.com/",
                LinkTwitter: "https://twitter.com"
            }
        }
    }
</script>

<style lang="sass" scoped>
    .footer
        display: flex
        flex: 0 0 auto
        box-sizing: border-box
        width: 100%
        height: 114px
        padding: 0 36px
        transition: transform .5s ease
        background-color: #F2F5FA
        align-items: center
        justify-content: space-between
        @media (max-width: 1366px)
            height: 80px
        @media (max-width: 768px)
            height: 65px
            font-size: .9em
        .scroll-down
            color: #818992
        .down-arrow
            width: 0
            height: 0
            margin: 0
            margin-left: -40px
            cursor: pointer
            transition: transform .5s ease
            border-width: 10px 10px 0 10px
            border-style: solid
            border-color: #2E363F transparent transparent transparent
        .social
            display: flex
            align-items: center
            justify-content: space-between
            min-width: 65px
            height: 25px
</style>
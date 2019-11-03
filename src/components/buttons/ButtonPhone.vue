<template>
    <div>
        <a :href="'tel:' + phone"  class="phone">
            <div>
                <div class="phone__icon">
                    <IconPhone class="iconPhone"/>
                </div>
            </div>

            <div class="phone_number">
                <slot />
            </div>
        </a>
    </div>
</template>

<script>
    import IconPhone from "@/components/icons/IconPhone";
    export default {
        name: "ButtonPhone",
        components: {IconPhone},
        props: {
            'phone': String
        }
    }
</script>

<style lang="sass" scoped>

    .phone
        display: flex
        text-decoration: none
        align-items: center
        font-family: 'Tinos'
        &:hover > .phone__icon
            background-color: rgba(216, 216, 216, 0.5)
        &:hover > .phone_number
            @media (min-width: 768px)
                margin-left: 40px

        .phone__icon
            display: flex
            justify-content: center
            align-items: center
            width: 40px
            height: 40px
            border: 1px solid #F2F5FA
            border-radius: 50%
            transition: background-color ease .5s
            background-color: transparent
            @media (max-width: 768px)
                height: 30px
                width: 30px
            .iconPhone
                @media (max-width: 768px)
                    height: 50%

        .phone_number
            padding: 15px 0
            margin-left: 30px
            transition: opacity ease .5s, margin ease .5s
            color: #94979E
            @media (max-width: 768px)
                font-size: .9em
                margin-left: 20px


</style>
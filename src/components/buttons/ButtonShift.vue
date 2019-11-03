<template>
    <div>
        <a :href="link"  :class="'button-shift ' + type">
            <div>
                <div class="icon">
                    <slot></slot>
                </div>
            </div>

            <div class="label">
                {{ label }}
            </div>
        </a>
    </div>
</template>

<script>
    export default {
        name: "ButtonShift",
        props: {
            'link': String,
            'label': String,
            'type': String
        }
    }
</script>

<style lang="sass" scoped>

    .button-shift
        display: flex
        text-decoration: none
        align-items: center
        font-family: 'Tinos'
        &:hover > .icon
            background-color: rgba(216, 216, 216, 0.5)
        &:hover > .label
            @media (min-width: 768px)
                margin-left: 40px

        .icon
            display: flex
            justify-content: center
            align-items: center
            width: 40px
            height: 40px;
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

        .label
            padding: 15px 0
            margin-left: 30px
            transition: opacity ease .5s, margin ease .5s
            color: #94979E
            @media (max-width: 768px)
                font-size: .9em
                margin-left: 20px

    /*.play*/
    /*    .icon*/
    /*        border-color: rgba(242, 245, 250, .3)*/


</style>
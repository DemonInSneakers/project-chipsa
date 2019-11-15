<template>
    <a class="button-shift" :href="link">
        <span class="icon">
            <slot></slot>
        </span>

        <span class="label">
            {{ label }}
        </span>
    </a>
</template>

<script>
    export default {
        name: "ButtonShift",
        props: {
            'link' : String,
            'label': String
        }
    }
</script>

<style lang="sass" scoped>

    .button-shift
        display: flex
        text-decoration: none
        outline: none
        align-items: center
        font-family: 'Tinos'
        cursor: pointer
        @media (min-width: 768px)
            &:hover
                .icon
                    background-color: rgba(216, 216, 216, 0.5)
            &:hover
                .label
                    margin-left: 40px
        @media (max-width: 768px)
            &:active
                .icon
                    background-color: rgba(216, 216, 216, 0.5)

        .icon
            display: flex
            flex: 0 0 auto
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
            svg
                height: 50%
        .label
            padding: 15px 0
            margin-left: 30px
            transition: opacity ease .5s, margin ease .5s
            color: #94979E
            @media (max-width: 768px)
                padding: 10px 0
                font-size: .9em
                margin-left: 20px


</style>
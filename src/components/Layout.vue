<template>
    <div class="layout">
        <Header />
        <Preloader />
        <slot />
        <Footer />
    </div>
</template>

<script>

    import Header from "@/components/Header";
    import Footer from "@/components/Footer";
    import Preloader from "@/components/Preloader";
    export default {
        name: "Layout",
        components: {
            Preloader,
            Footer,
            Header
        }
    }
</script>

<style scoped>
    .layout {
        display: flex;
        flex-direction: column;

        background-color: #394551;
        background-image: url('../assets/main-bg.jpg');
        background-repeat: repeat;
        position: relative;
        overflow: hidden;
        height: 100vh;
        width: 100%;
    }
</style>



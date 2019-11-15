<template>
  <div id="app">
    <Pages />
  </div>
</template>

<script>


import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
import MQ from 'vue-match-media/src'
import Pages from "@/components/Pages"

import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
import 'reset-css/reset.css'
import './styles/reset-button.css'
import './fonts/Roboto.css'
import './fonts/Tinos.css'

Vue.use(BootstrapVue)
Vue.use(MQ)

export default {
  name: 'app',
  components: {
    Pages
  },
  mq: {
    phone: '(min-width: 768px)',
    tablet: '(max-width: 1366px)',
    desktop: '(min-width: 1366px)'
  }
}
</script>

<style lang="sass">

</style>

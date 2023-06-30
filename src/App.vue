<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import BlueBand from './components/BlueBand.vue'

import { blueMenu, dcComics, footerMenu, navElements, socialMenu, } from './assets/data/index';

export default {
  name: 'DC Comics',
  components: { AppHeader, AppMain, AppFooter, BlueBand },
  data() {
    return {
      blueMenu,
      dcComics,
      footerMenu,
      navElements,
      socialMenu,
    }
  }
}

</script>

<template>
  <AppHeader :nav-Elements="navElements" />
  <AppMain />
  <BlueBand />
  <AppFooter :social-menu="socialMenu" :footer-Menu="footerMenu" />
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>

<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import BlueBand from './components/BlueBand.vue'

export default {
  name: 'DC Comics',
  components: { AppHeader, AppMain, AppFooter, BlueBand }
}

</script>

<template>
  <AppHeader />
  <AppMain />
  <BlueBand />
  <AppFooter />
</template>

<style></style>

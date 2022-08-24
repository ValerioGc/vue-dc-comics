<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <AppHeader />
    <AppMain />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from './components/appHeader.vue';
import AppFooter from './components/appFooter.vue';
import AppMain from './components/appMain.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    AppMain
  }
}
</script>

<style lang="scss">

</style>

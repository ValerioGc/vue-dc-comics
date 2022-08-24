<template>
  <div id="app">
    <appHeader />
    <appMain />
    <appFooter />
  </div>
</template>

<script>
  import appHeader from './components/appHeader.vue';
  import appMain from './components/appMain.vue';
  import appFooter from './components/appFooter.vue';
  
  export default {
    name: 'App',
    components: {
      appHeader,
      appMain,
      appFooter
    }
  }
</script>

<style lang="scss"></style>

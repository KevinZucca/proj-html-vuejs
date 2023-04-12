<script>
import AppHeader from './components/AppHeader_components/AppHeader.vue';
import AppMain from './components/AppMain_components/AppMain.vue';
import AppFooter from './components/AppFooter_components/AppFooter.vue';
import Copyright from './components/Copyright.vue';

export default {
  data() {
    return {

    }
  },

  components: {
    AppHeader,
    AppMain,
    AppFooter,
    Copyright,
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
  <AppFooter></AppFooter>
  <Copyright></Copyright>

</template>

<style scoped>
</style>

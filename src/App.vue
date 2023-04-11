<script>
import AppHeader from './components/AppHeader_components/AppHeader.vue';
import AppMain from './components/AppMain_components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';


export default {
  data() {
    return {

    }
  },

  components: {
    AppHeader,
    AppMain,
    AppFooter,
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
  <AppFooter></AppFooter>

</template>

<style scoped>
</style>

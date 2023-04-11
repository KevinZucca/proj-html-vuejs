<script>
import AppHeaderNavbar from './AppHeaderNavbar.vue';
import AppHeaderJumbo from './AppHeaderJumbo.vue';

export default {

    data() {
        return {
            name: "AppHeader",

        }
    },

    components: {
        AppHeaderNavbar,
        AppHeaderJumbo,
    }
}
</script>

<template>
    <AppHeaderNavbar></AppHeaderNavbar>
    <AppHeaderJumbo></AppHeaderJumbo>
</template>

<style scoped>

</style>

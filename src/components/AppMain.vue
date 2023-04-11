<script>
import AppMain_Section1 from './AppMain_Sections/AppMain_Section1.vue';
import AppMain_Section2 from './AppMain_Sections/AppMain_Section2.vue';
import AppMain_Section3 from './AppMain_Sections/AppMain_Section3.vue';
import AppMain_Section4 from './AppMain_Sections/AppMain_Section4.vue';
import AppMain_Section5 from './AppMain_Sections/AppMain_Section5.vue';
import AppMain_Section6 from './AppMain_Sections/AppMain_Section6.vue';
import AppMain_Section7 from './AppMain_Sections/AppMain_Section7.vue';
import AppMain_Section8 from './AppMain_Sections/AppMain_Section8.vue';
import AppMain_Section9 from './AppMain_Sections/AppMain_Section9.vue';


export default {

    data() {
        return {
            name: "AppMain",

        }
    },

    components: {
        AppMain_Section1,
        AppMain_Section2,
        AppMain_Section3,
        AppMain_Section4,
        AppMain_Section5,
        AppMain_Section6,
        AppMain_Section7,
        AppMain_Section8,
        AppMain_Section9,
   }
}
</script>

<template>
    <AppMain_Section1></AppMain_Section1>
    <AppMain_Section2></AppMain_Section2>
    <AppMain_Section3></AppMain_Section3>
    <AppMain_Section4></AppMain_Section4>
    <AppMain_Section5></AppMain_Section5>
    <AppMain_Section6></AppMain_Section6>
    <AppMain_Section7></AppMain_Section7>
    <AppMain_Section8></AppMain_Section8>
    <AppMain_Section9></AppMain_Section9>
</template>

<style scoped>

</style>

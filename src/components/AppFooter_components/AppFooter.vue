<script>
import FooterAboutItem from './FooterAboutItem.vue';
import FooterTwitterItem from './FooterTwitterItem.vue';
import FooterLinks from './FooterLinksItem.vue';
import FooterContact from './FooterContact.vue';

export default {

    data() {
        return {
            name: "AppFooter",

        }
    },

    components: {
        FooterAboutItem,
        FooterTwitterItem,
        FooterLinks,
        FooterContact,
    }
}
</script>

<template>
   <div class="main-container">
        <div class="container-centered">
            <FooterAboutItem></FooterAboutItem>
            <FooterTwitterItem></FooterTwitterItem>
            <FooterLinks></FooterLinks>
            <FooterContact></FooterContact>
        </div>
    </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 550px;

        background-color: #181515;

        .container-centered {
            display: flex;
            align-items: center;
            gap: 50px;
        }
    }
</style>

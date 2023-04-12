<script>

export default {

    data() {
        return {
            name: "FooterAboutItem",

        }
    },
}
</script>

<template>
    <div id="column">
        <div class="title">
            <h2>About</h2>
        </div>
        <div id="description">
            <p class="grey-text">
                We created Everlead to effectively become the stepping stone towards meeting all your goals & achieving business success.
            </p>
        </div>
        <div id="social-icons">
            <i class="fa-brands fa-linkedin-in"></i>
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-twitter"></i>
        </div>
    </div>

</template>

<style scoped lang="scss">
  #column {
        display: flex;
        flex-flow: column;

        height: 300px;
        width: 100%;

        .title {
            color: white;
        }

        .title::after {
            content: '';
            height: 2px;
            width: 35px;

            background-color: #ff4612;
            display: block;

            margin: 10px 0
        }

        #social-icons {
            display: flex;
            gap: 10px;
        }

        #social-icons i {
            border-radius: 15px;

            margin-top: 15px;
            padding: 5px;
            width: 26px;

            text-align: center;

            background-color: white;
            color: #181515;
        }
    }
</style>

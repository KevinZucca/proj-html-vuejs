<script>
export default {

    data() {
        return {
            name: "AppHeaderNavbar",
        }
    },
}
</script>

<template>
    <div class="main-container">
        <div id="logo">
            <a href="#">LOGO</a>
        </div>
        <div id="links">
            <ul>
                <li><a href="#">link</a></li>
                <li><a href="#">link</a></li>
                <li><a href="#">link</a></li>
                <li><a href="#">link</a></li>
                <li><a href="#">link</a></li>
                <li><a href="#">link</a></li>
                <li><a href="#">link</a></li>
                <li><a href="#">link</a></li>
            </ul>
        </div>
    </div>
</template>

<style scoped lang="scss">
    .main-container {
        height: 75px;
        
        justify-content: space-between;
        align-items: center;

        background-color: gray;

        ul {
            display: flex;
            gap: 10px;

            text-transform: uppercase;

        }

        a {
            text-decoration: none;
            color: black;
        }
    }
</style>

<script>

export default {

    data() {
        return {
            name: "AppMain_Section7",

        }
    },
}
</script>

<template>
   <div class="main-container">
    <div id="picture-container">
        <img class="big-wallpaper" src="/public/img/h1-img-04.jpg" alt="big-wallpaper">
        <div id="play-button">
            <i class="fa-solid fa-play"></i>
        </div>
    </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 800px;

        background-color: rgba(104, 234, 195, 0.662);

        padding: 0;
        position: relative;

        #picture-container {
            display: flex;
            flex-flow: row nowrap;

            width: 100%;
            height: 100%;

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }

            #play-button {
                color: white;
                font-size: 3em;

                cursor: pointer;

                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);

            }
        }
    }
</style>

<script>

export default {

    data() {
        return {
            name: "AppMain_Section7",
            isLoading: false,
            showPlayer: true,
        }
    },
}
</script>

<template>
   <div class="main-container">
    <div id="picture-container">
        <img class="big-wallpaper" src="/public/img/h1-img-04.jpg" alt="big-wallpaper">
        <div @click="isLoading = true, showPlayer = false" id="play-button" v-show="showPlayer">
            <i class="fa-solid fa-play"></i>
        </div>

        <span v-show="isLoading" id="loader"></span>
        
    </div>
   </div>
</template>

<style scoped lang="scss">

// LOADER ANIMATIONS 
@keyframes rotate {
    0% { transform: rotate(0deg) scale(0.8) }
    50% { transform: rotate(360deg) scale(1.2) }
    100% { transform: rotate(720deg) scale(0.8) }
}

@keyframes ball1 {
    0% {
     box-shadow: 30px 0 0 #ff3d00;
    }
    50% {
        box-shadow: 0 0 0 #ff3d00;
        margin-bottom: 0;
        transform: translate(15px, 15px);
    }
    100% {
        box-shadow: 30px 0 0 #ff3d00;
        margin-bottom: 10px;
    }
}

@keyframes ball2 {
    0% {
        box-shadow: 30px 0 0 #fff;
    }
    50% {
        box-shadow: 0 0 0 #fff;
        margin-top: -20px;
        transform: translate(15px, 15px);
    }
    100% {
        box-shadow: 30px 0 0 #fff;
        margin-top: 0;
    }

    // /LOADER ANIMATIONS



    }
    .main-container {
        width: 100%;
        height: 800px;

        padding: 0;
        position: relative;

        #picture-container {
            display: flex;
            flex-flow: row nowrap;

            width: 100%;
            height: 100%;

            #loader {
                position: absolute;
                top: 47%;
                left: 48.5%;
                transform: translate(-50%, -50%);

                width: 50px;
                height: 50px;

                animation: rotate 1s infinite;

                &:before,
                &:after {
                    border-radius: 50%;
                    content: "";
                    display: block;
                    height: 20px;
                    width: 20px;
                 }

              
                &:before {
                    animation: ball1 1s infinite;
                    background-color: #fff;
                    box-shadow: 30px 0 0 #ff3d00;
                }

                &:after {
                    animation: ball2 1s infinite;
                    background-color: #ff3d00;
                    box-shadow: 30px 0 0 #fff;
                }

            }  

            &:hover img {
                 filter: brightness(80%);
                }


            img {
                width: 100%;
                height: 100%;
                object-fit: cover;

                filter: brightness(90%);
                transition: all .2s ease;
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

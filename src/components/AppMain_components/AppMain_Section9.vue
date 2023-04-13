<script>

export default {

    data() {
        return {
            name: "AppMain_Section9",
            logos: [
                "/public/img/h4-clients-img-03.png",
                "/public/img/h4-clients-img-05.png",
                "/public/img/h4-clients-img-07.png",
                "/public/img/h4-clients-img-09.png",
                "/public/img/h4-clients-img-01.png",
            ],
        }
    },
}
</script>

<template>
   <div class="main-container">
    <div class="container-centered">
        <div class="logo" v-for="logo in logos">
            <a href="#"><img :src="logo" alt="logo"></a>
        </div>
    </div>
   </div>
</template>

<style  lang="scss">
    .main-container {
        width: 100%;
        height: 200px;

        background-color: #fafafafa;

        .container-centered {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 120px;

            .logo {
            height: 100%;
            width: calc(100% / 5);
            transition: all .3s ease;

            cursor: pointer;

            &:hover {
                scale: 1.3;
            }
        }
        }
       
    }
</style>

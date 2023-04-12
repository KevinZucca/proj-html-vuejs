<script>

export default {

    data() {
        return {
            name: "AppMain_Section6",
            profiles: [
                {
                    img: "/public/img/h3-img-04.png",
                    name: "Cynthia Clark",
                    cit: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed eiusmod tempor indicididunt ut labore et dolore magna aliqua",
                },
                {
                    img: "/public/img/h3-img-07.png",
                    name: "Janeth Xyn",
                    cit: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed eiusmod tempor indicididunt ut labore et dolore magna aliqua",
                },
                {
                    img: "/public/img/h3-img-08.png",
                    name: "Amanda Graph",
                    cit: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed eiusmod tempor indicididunt ut labore et dolore magna aliqua",
                },
            ]

        }
    },
}
</script>

<template>
   <div class="main-container">
    <div class="left-arrow arrow">
        &leftarrow;
    </div>
    <div class="right-arrow arrow">
        &rightarrow;
    </div>

    <div class="container-centered">
        <div class="card-container"  v-for="profile in profiles">
            <div class="card">
                <div class="profile-img">
                    <img :src="profile.img" alt="profile-img">
                </div>
                <h4 class="name title white-text">{{ profile.name }}</h4>
                <p class="cit subtitle">"{{ profile.cit }}""</p>
            </div>
        </div>
    </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 450px;

        background-color: #1e1c1c;
        position: relative;

        .arrow {
            position: absolute;
            color: white;

            &.left-arrow {
                top: 50%;
                left: 10px;
            }

            
            &.right-arrow {
                top: 50%;
                right: 10px;
            }
        }

        .container-centered {
            display: flex;
            flex-flow: row nowrap;
            justify-content: flex-start;
            align-items: center;
            gap: 100px;

            text-align: center;
            width: 500px;

            overflow-x: scroll;

            .card {
                width: 500px;
            }

            }
        }
</style>

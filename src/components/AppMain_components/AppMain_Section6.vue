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
            ],

            mainIndex: 0,


        }
    },

    methods: {
        slideToLeft() {
            document.querySelector(".card-container").scrollBy({
            left: 650, 
            behavior: "smooth"
            })

            this.mainIndex++
            if(this.mainIndex >= this.profiles.length){
                this.mainIndex = 0
            }
        },

        slideToRight() {
            document.querySelector(".card-container").scrollBy({
            left: -650, 
            behavior: "smooth"
            })
            this.mainIndex--
            if(this.mainIndex < 0){
                this.mainIndex = 2
            }
        },

    },

}
</script>

<template>
   <div class="main-container">
    <div class="left-arrow arrow" @click="slideToRight()">
        &leftarrow;
    </div>
    <div class="right-arrow arrow" @click="slideToLeft()">
        &rightarrow;
    </div>

    <div class="container-centered">
        <div class="card-container">
            <div class="card" v-for="(profile,index) in profiles" :key="index">
                <div class="profile-img">
                    <img :src="profiles[this.mainIndex].img" alt="profile-img">
                </div>
                <h4 class="name title white-text">{{ profiles[this.mainIndex].name }}</h4>
                <p class="cit subtitle">"{{ profiles[this.mainIndex].cit }}"</p>
            </div>
        </div>
    </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 400px;

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
            width: 600px;

            .card-container {
                height: 70%;
                
                display: flex;
                gap: 50px;

                overflow-x: hidden;

            }

            .card {
                width: 600px;

                display: flex;
                flex-flow: column;
                align-items: center;
                flex-shrink: 0;

                text-align: center;
            }
        }
    }
</style>

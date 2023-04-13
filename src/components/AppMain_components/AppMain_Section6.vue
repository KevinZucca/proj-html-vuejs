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
            let indexBar = document.querySelector("#index-bar");

            document.querySelector(".card-container").scrollBy({
            left: 650, 
            behavior: "smooth"
            })
            this.mainIndex++;
            if(this.mainIndex >= this.profiles.length) {
                this.mainIndex = 0;
                document.querySelector(".card-container").scrollBy({
                left: -1350, 
                behavior: "smooth"
                })
                indexBar.style.left = ("0px")
            }

           
            if(this.mainIndex == 1){
                indexBar.style.left = ("50px")
            } else if (this.mainIndex == 2){
                indexBar.style.left = ("100px")
            }
        },

        slideToRight() {
            document.querySelector(".card-container").scrollBy({
            left: -650, 
            behavior: "smooth"
            })
            this.mainIndex--;
            if(this.mainIndex < 0) {
                this.mainIndex = 0
            }

            let indexBar = document.querySelector("#index-bar");
            if(this.mainIndex == 0){
                indexBar.style.left = ("0px")
            } else if (this.mainIndex == 1) {
                indexBar.style.left = ("50px")
            }
        },
    },

    mounted() {
        setInterval(() => {
            this.slideToLeft()
        }, 4000);
    }
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
        <div id="index-container">
            <p>{{ mainIndex + 1}}</p>
            <div id="bar">
                <div id="index-bar"></div>
            </div>
            <p>3</p>
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
            flex-flow: column;
            gap: 0;

            .card-container {
                height: 70%;
                width: 100%;
                
                display: flex;
                align-items: center;
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

            #index-container {
                display: flex;
                justify-self: flex-start;
                justify-content: space-between;
                align-items: center;
                gap: 8px;
                flex-grow: 1;

                color: #bdbdbd;

                #bar {
                    width: 150px;
                    height: 3px;

                    background-color: #ffffff2c;

                    border-radius: 2px;

                    #index-bar {
                        width: 33%;
                        height: 100%;

                        background-color: rgb(255, 255, 255);

                        position: relative;
                    }
                }

                
            }
        }
    }
</style>

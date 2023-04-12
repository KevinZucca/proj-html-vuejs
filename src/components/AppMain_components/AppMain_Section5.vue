<script>

export default {

    data() {
        return {
            name: "AppMain_Section5",
            businessCards: [ 
                {
                    picture1: "/public/img/h1-blog-img-01.jpg",
                    time: "May 5, 2019",
                    person: "Amanda Doe",
                    name: "Next investment",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, seid eius mas tellus dolor ...",
                    moreInfo: "READ MORE",
                },
                {
                    picture1: "/public/img/h1-blog-img-02.jpg",
                    time: "May 5, 2019",
                    person: "Amanda Doe",
                    name: "Team Building",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, seid eius mas tellus dolor ...",
                    moreInfo: "READ MORE",
                },
                {
                    picture1: "/public/img/h1-blog-img-03.jpg",
                    time: "May 5, 2019",
                    person: "Amanda Doe",
                    name: "New Business Day",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, seid eius mas tellus dolor ...",
                    moreInfo: "READ MORE",
                },
                {
                    picture1: "/public/img/h1-blog-img-04.jpg",
                    time: "May 5, 2019",
                    person: "Amanda Doe",
                    name: "Project Reunions",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, seid eius mas tellus dolor ...",
                    moreInfo: "READ MORE",
                }
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
            <div id="comment">
                <div class="title">
                    <h2>Latest news<span class="orange-dot">.</span></h2>
                </div>
                <div id="description">
                    <p class="grey-text">Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
                </div>
            </div>

            <div id="business-container">
                <div class="card" v-for="business in businessCards">
                    <div class="img-container">
                        <img :src="business.picture1" alt="up-img">
                        <div class="sticker">
                            <span><i class="fa-solid fa-tag"></i></span>
                            <p>Business, Leading</p>
                        </div>
                    </div>
                    
                    <div class="card-text">
                        <div class="info">
                            <span class="clock"><i class="fa-regular fa-clock"></i></span>
                            <p class="time subtitle">{{ business.time }}</p>
                            <span class="user"><i class="fa-regular fa-user"></i></span>
                            <p class="person subtitle">{{ business.person }}</p>
                        </div>
                       
                        <h3 class="title">{{ business.name }}</h3>
                        <p class="subtitle">{{ business.description }}</p>
                        <strong>{{ business.moreInfo }}</strong>
                    </div>
                    
                </div>
            </div>
        </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 700px;

        background-color: #fafafa;
        background-image: url("/public/svg/svg-4.svg");
        background-size: 400px;
        background-repeat: no-repeat;
        background-position: top -150px left 0;

        margin-bottom: 50px;
        padding-top: 0;

        position: relative;


        .arrow {
            position: absolute;

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
            flex-flow: column;
            gap: 0;
            
            width: 100%;


        #comment {
                display: flex;
                flex-flow: column;
                justify-content: center;
                align-items: center;

                padding: 50px;
                height: 30%;
            
                .title {
                    font-size: 1.8em;
                }

                #description::after {
                    content: '';
                    height: 2px;
                    width: 75px;

                    background-color: #ff4612;
                    display: block;

                    margin: 0 auto;
                    margin-top: 20px;
                }
            }

            #business-container {
                display: flex;
                gap: 30px;

                width: 100%;
                height: 70%;
                overflow-x: scroll;

                .card {
                    display: flex;
                    flex-flow: column;
        
                    width: 31%;

                    .img-container {
                        display: flex;
                        flex-flow: column;

                        width: 100%;
                        position: relative;

                        .sticker {
                            display: flex;
                            gap: 5px;
                            background-color: #ff4612;
                            color: white;

                            position: absolute;
                            bottom: -10px;
                            right: 15px;

                            padding: 10px;
                        }
                    }

                    .card-text {
                        display: flex;
                        flex-flow: column;

                        padding: 10px 0;


                        .info {
                            display: flex;
                            align-items: center;

                            font-size: 1em;

                            p {
                                margin-right: 10px;
                            }

                            i {
                                font-size: .8em;
                                margin-right: 5px;
                                color: #ff4612;
                            }
                        }

                        .title {
                            font-size: 1.3em;
                        }
                    }
                }
            }
        }

    }
</style>

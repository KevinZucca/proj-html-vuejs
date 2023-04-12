<script>

export default {

    data() {
        return {
            name: "AppMain_Section5",
            businessCards: [ 
                {
                    picture1: "/public/img/h1-blog-img-02.jpg",
                    picture2: "/public/img/h1-blog-img-03.jpg",
                    time: "May 5, 2019",
                    person: "Amanda Doe",
                    name: "Next investment",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, seid eius mas tellus dolor ...",
                    moreInfo: "READ MORE",
                },
                {
                    picture1: "/public/img/h1-blog-img-03.jpg",
                    picture2: "/public/img/h1-blog-img-01.jpg",
                    time: "May 5, 2019",
                    person: "Amanda Doe",
                    name: "Team Building",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, seid eius mas tellus dolor ...",
                    moreInfo: "READ MORE",
                },
                {
                    picture1: "/public/img/h1-blog-img-01.jpg",
                    picture2: "/public/img/h1-blog-img-02.jpg",
                    time: "May 5, 2019",
                    person: "Amanda Doe",
                    name: "New Business Day",
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
                        <img class="up-img" :src="business.picture1" alt="up-img">
                        <img class="down-img" :src="business.picture2" alt="down-img">
                    </div>
        
                    <div id="time" class="subtitle"></div> <span class="subtitle"></span>
                    <div class="title"></div>
                    <div class="subtitle"></div>
                    <div class="more-info"></div>
                </div>
            </div>
        </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 600px;

        background-color: rgb(244, 198, 112);
        padding-top: 0;

        .container-centered {
            flex-flow: column;
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

                .card {
                    display: flex;
                    flex-flow: column;
        
                    width: 30%;
                    height: 100%;
                    background-color: white;

                    .img-container {
                        display: flex;
                        flex-flow: column;

                        width: 100%;
                        height: 900px;

                        .up-img {
                            height: 150px;
                            object-fit: cover;
                            overflow: hidden;
                        }

                        .down-img {
                            height: 150px;
                            object-fit: cover;
                            overflow: hidden;
                        }


                    }
                }
            }
        }

    }
</style>

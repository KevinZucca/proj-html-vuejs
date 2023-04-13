<script>

export default {

    data() {
        return {
            name: "AppMain_Section4",
            percentages: [
                {
                    type: "Mentorship",
                    number: "78%",
                },
                {
                    type: "Education",
                    number: "95%",
                },
                {
                    type: "Learning",
                    number: "65%",
                },
                {
                    type: "Motivation",
                    number: "83%",
                },
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
                    <h2>Creative Leader<span class="orange-dot">.</span></h2>
                </div>
                <div id="description">
                    <p class="grey-text">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Cumque expedita amet repellat sequi autem non explicabo eum nihil recusandae eius delectus placeat facilis consequatur praesentium sunt, provident repudiandae quibusdam nobis.</p>
                </div>
                <strong>
                    <a href="#" class="read-more">READ MORE</a>
                </strong>
            </div>


            <div id="percentages">
                <div class="row" v-for="percentage in percentages">
                    <div class="title">
                        {{ percentage.type }}
                    </div>
                    <div class="percent">
                        {{ percentage.number }}
                    </div>
                    <div class="bar">
                        <div class="filled-bar" :style="{ width: percentage.number }">
                        </div>
                    </div>
                </div>
            </div>

        </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 400px;

        background: #ffffff;


        .container-centered {
            display: flex;
            gap: 50px;

        #comment {
                display: flex;
                flex-flow: column;
                justify-content: center;

                padding: 50px;
                height: 350px;
                width: 50%;

                .title {
                    font-size: 1.5em;
                }

                .title::after {
                    content: '';
                    height: 2px;
                    width: 75px;

                    background-color: #ff4612;
                    display: block;

                    margin: 15px 0;
                }

                #description {
                    margin-bottom: 20px;
                }

            }

            #percentages {
                display: flex;
                flex-flow: column;
                justify-content: space-between;
                gap: 20px;

                padding: 75px;
                height: 350px;
                width: 50%;

                .row {
                    display: flex;
                    flex-flow: row wrap;
                    justify-content: space-between;

                    font-size: 1.2em;
                    font-weight: bold;

                    .title {
                        flex-grow: 1;
                    }

                    .bar {
                        width: 100%;
                        height: 3px;
                        background-color: rgba(0, 0, 0, 0.084);

                        .filled-bar {
                            height: 100%;
                            background-color: #ff4612;
                            animation: fill 6s infinite;

                                @keyframes fill {
                                from {
                                    width: 0%;
                                } to {
                                }
                            }
                               
                        }
                    }

                    
                }
            }
        }

    }
</style>

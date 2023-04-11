<script>

export default {

    data() {
        return {
            name: "AppMain_Section2",

        }
    },
}
</script>

<template>
   <div class="main-container">
    <div class="container-centered">
        <div id="photo">
            <img src="public/img/h1-img-01.jpg" alt="individual-reunion-img">
            <div id="arrows">
                <p>&leftarrow;</p>
                <p>&rightarrow;</p>
            </div>
        </div>
        <div id="comment">
            <div class="title">
                <h2>Jason Bickford</h2>
            </div>
            <div class="subtitle">
                <p>Founder and Executive Director</p>
            </div>
            <div class="description">
                <p class="grey-text">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati dolorum nesciunt exercitationem quas, saepe atque. Repudiandae natus</p>
            </div>
            <div id="social-icons">
                <i class="fa-brands fa-linkedin-in"></i>
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
            </div>
        </div>
    </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 450px;
        
        margin: 100px 0;

        background-image: url("public/svg/svg-4.svg");
        background-repeat: no-repeat;
        background-position: right 200px bottom 80px;
        background-size: 350px;

        .container-centered {   
            display: flex;
            align-items: center;

            height: 100%;
            width: 100%;

            #photo {
                width: 80%;
                height: 100%;

                position: relative;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                }

                #arrows {
                    display: flex;
                    align-items: center;
                    justify-content: center;

                    width: 120px;

                    font-size: 1.5em;
                    position: absolute;
                    bottom: 0;
                    left: 0;

                    background-color: #ff4612;
                    color: white;

                    padding: 10px;
                    cursor: pointer;

                    p {
                        margin: 0 10px;
                    }
                }
            }

            #comment {
                display: flex;
                flex-flow: column;
                justify-content: center;

                padding: 50px;
                height: 350px;

                margin-left: -40px;
                z-index: 2;

                background-color: #fff;
                .title {
                    font-size: 1.5em;
                }

                .subtitle {
                    font-size: .9em;
                }

                .subtitle::after {
                    content: '';
                    height: 2px;
                    width: 75px;

                    background-color: #ff4612;
                    display: block;

                    margin: 15px 0;
                }

                #social-icons {
                    display: flex;
                    gap: 10px;
                }

                #social-icons i {
                    border-radius: 15px;

                    margin-top: 15px;
                    padding: 5px;
                    width: 26px;

                    text-align: center;

                    background-color: #ff4612;
                    color: white;
                }
            }

        }
    }
</style>

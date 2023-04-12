<script>
export default {

    data() {
        return {
            name: "AppHeaderJumbo",
        }
    },

    components: {
    },

    methods: {
        nextPicture() {
            document.querySelector("#jumbo-carousel").scrollBy({
            left: -550, 
            behavior: "smooth"
            })
        },
    }
}
</script>

<template>
    <div class="main-container">
        <div id="jumbo-carousel">
            <img class="jumbo-img" src="/public/img/rev-slider-main-home-img-03.jpg" alt="jumbo-img">
            <img class="jumbo-img" src="/public/img/rev-slider-main-home-img-02.png" alt="jumbo-img">
        </div>
        
        <!-- NAVBAR -->
        <nav>
            <div id="logo">
                <a href="#"><img src="/public/img/logo-img-01.png" alt="nav-logo"></a>
            </div>
        <div id="links">
            <ul>
                <li><a href="#">homes</a></li>
                <li><a href="#">pages</a></li>
                <li><a href="#">block</a></li>
                <li><a href="#">shop</a></li>
                <li><a href="#">events</a></li>
                <li><a href="#">elements</a></li>
                <li><a href="#"><i class="fa-solid fa-magnifying-glass fa-flip-horizontal"></i></a></li>
                <li><a href="#"><i class="fa-solid fa-list"></i></a></li>
            </ul>
        </div>
        </nav>
        <!-- //NAVBAR -->

        
        <!-- LEFT ARROW SLIDER -->
        <div class="arrow left-arrow">
            <a href="#">&leftarrow;</a>
        </div>
        <!-- //LEFT ARROW SLIDER -->


        <!-- JUMBO MAIN CONTENT -->
        <div id="intro" class="container">
            <h1>Our Team<span class="orange-dot">.</span></h1>
            <p class="subtitle">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam.</p>
            <div id="buttons-container">
                <button>
                    <p>READ MORE</p>
                    <span>&rightarrow;</span>
                </button>
                <button class="orange-button">
                    <p>PURCHASE</p>
                    <span>&rightarrow;</span>
                </button>
            </div>
        </div>
        <!--//JUMBO MAIN CONTENT  -->


        <!-- RIGHT ARROW SLIDER -->
        <div @click="nextPicture()" class="arrow right-arrow">
            <a href="#">&rightarrow;</a>
        </div>
        <!-- //RIGHT ARROW SLIDER -->

    </div>
</template>

<style scoped lang="scss">
    .main-container {
        height: 750px;

        flex-flow: column;  
        gap: 250px;  
        position: relative;

        padding: 0;

        #jumbo-carousel {
            display: flex;
            flex-flow: row nowrap;

            width: 200vw;
            height: 100%;

            pointer-events: none;

            .jumbo-img {
                width: 2500px;
                height: 100%;
                object-fit: cover;
            }
        }

        nav {
            width: 100%;
            height: 75px;
            padding: 20px;

            display: flex;
            justify-content: space-between;
            align-items: center;

            font-weight: 500;

            position: absolute;

                #logo img {
                    width: 120px;
                }

                ul {
                    display: flex;
                    gap: 40px;

                    text-transform: uppercase;

                }

                a {
                    text-decoration: none;
                    color: black;
                }
            }

        #intro {
            max-width: 600px;
            font-size: 1.5em;

            position: absolute;
            top: 60%;
            left: 30%;
            transform: translate(-50%, -50%);


            h1 {
                font-size: 3em;
                font-weight: 600;

                font-family: serif;
            }

            #buttons-container {
                display: flex;
                gap: 15px;

                padding: 30px 0;

                button {
                   
                    p {
                        width: 80%;
                        border-right: 0.5px solid;
                    }
                }
            }
        }

        .arrow {
            position: absolute;

            font-size: 20px;

            & a {
                text-decoration: none;
                color: #6a6a6a;

                font-size: 2em;
            }
            &.left-arrow {
                left: 10px;
                top: 50%;
            }

            &.right-arrow {
                right: 10px;
                top: 50%;
            }

        }
    }
</style>

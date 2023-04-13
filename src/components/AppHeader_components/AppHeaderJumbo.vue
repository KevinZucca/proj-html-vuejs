<script>
export default {

    data() {
        return {
            name: "AppHeaderJumbo",
            photos: [
                "/public/img/rev-slider-main-home-img-02.png",
                "/public/img/rev-slider-main-home-img-03.jpg",
            ],

            maiIndex: 0,
        }
    },

    methods: {
        prevPicture() {
            this.maiIndex--;
            if(this.maiIndex < 0 ){
                this.maiIndex = this.photos.length - 1;
            }
        },

        nextPicture() {
            this.maiIndex++;
            if(this.maiIndex >= this.photos.length){
                this.maiIndex = 0;
            }
        },

        reloadPage() {
            window.location.reload()
        },

        scrollFunction() {
            let mybutton = document.querySelector("#myBtn");

            if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
                mybutton.style.display = "block";
            } else {
                mybutton.style.display = "none";
            }
        },

        topFunction() {
            document.body.scrollTop = 0;
            document.documentElement.scrollTop = 0;
        }
    },

    mounted() {
        window.onscroll = () => {
            this.scrollFunction()},

        setInterval(() => {
            this.nextPicture()
        }, 4000);
    }
}
</script>

<template>
    <div class="main-container">

        <!-- SCROLL TO TOP BUTTON -->
        <button @click="topFunction()" id="myBtn">&ShortUpArrow;</button>
        <!-- / SCROLL TO TOP BUTTON -->


        <div id="jumbo-carousel">
            <img class="jumbo-img" :src="this.photos[maiIndex]" alt="jumbo-img">
        </div>
        
        <!-- NAVBAR -->
        <nav>
            <div id="logo" @click="reloadPage()">
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
        <div @click="prevPicture()" class="arrow left-arrow">
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

        #myBtn {
            display: none;
            position: fixed;
            bottom: 40px;
            right: 30px;

            width: 80px;
            height: 60px;

            z-index: 5;
            font-size: 18px;
            border: 1px solid rgba(0, 0, 0, 0.112);

            background-color: white;
            color: #ff4612;

            cursor: pointer;

            padding: 10px;
            border-radius: 4px;

            font-size: 30px;
        }

        #jumbo-carousel {
            display: flex;
            flex-flow: row nowrap;

            width: 100%;
            height: 100%;

            pointer-events: none;

            .jumbo-img {
                width: 100%;
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
                    transition: .2s color ease-in;

                    &:hover {
                        color: #ff4612;
                        text-shadow: 3px 3px 4px rgba(0, 0, 0, 0.295);
                    }
                }
            }

        #intro {
            max-width: 600px;
            font-size: 1.5em;

            position: absolute;
            top: 60%;
            left: 30%;
            transform: translate(-50%, -50%);
            animation: appear 1.5s ease-in;

            @keyframes appear {
                from {
                    opacity: 0%;
                } to {
                    opacity: 100%;
                }
            }


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

                    &:hover p {
                        border-right: 0px;
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

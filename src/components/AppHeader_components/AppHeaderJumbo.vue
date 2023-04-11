<script>
export default {

    data() {
        return {
            name: "AppHeaderJumbo",

        }
    },

    components: {
    },
}
</script>

<template>
    <div class="main-container">
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
        <div class="arrow left-arrow">
            <a href="#">&leftarrow;</a>
        </div>
        <div id="intro" class="container">
            <h1>Our Team<span id="dot">.</span></h1>
            <p id="intro-parag">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam.</p>
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
        <div class="arrow right-arrow">
            <a href="#">&rightarrow;</a>
        </div>
    </div>
</template>

<style scoped lang="scss">
    .main-container {
        height: 800px;

        flex-flow: column;  
        gap: 250px;  
        position: relative;

        padding: 0 50px;

        background-image: url("/public/img/rev-slider-main-home-img-03.jpg");
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;

        nav {
            width: 100%;
            height: 75px;
            
            display: flex;
            justify-content: space-between;
            align-items: center;

            font-weight: 500;

                #logo img {
                    width: 70px;
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
            max-width: 750px;
            font-size: 1.5em;

            padding: 0 100px;

            #dot {
                color: #ff4612;
            }

            h1 {
                font-size: 3em;
                font-weight: 600;

                font-family: serif;
            }

            #intro-parag {
                color: #a6a6a6;
            }

            #buttons-container {
                display: flex;
                gap: 15px;

                padding: 30px 0;

                button {
                    width: 130px;
                    height: 35px;
                    
                    display: flex;
                    align-items: center;
                    justify-content: space-between;

                    cursor: pointer;
                    border: none;

                    padding: 8px;
                    background-color: white;

                    font-size: 0.4em;

                    &.orange-button {
                        background-color: #ff4612;
                        color: white;
                    }

                    p {
                        width: 80%;
                        border-right: 0.5px solid;
                    }
                }
            }
        }

        .arrow {
            position: absolute;

            & a {
                text-decoration: none;
                color: black;

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

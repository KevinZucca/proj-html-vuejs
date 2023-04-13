<script>

export default {

    data() {
        return {
            name: "AppMain_Section8",
            showMessage: false,

        }
    },

    methods: {
        usClicked() {
            let newYork = document.querySelector("#new-york");
            newYork.classList.toggle("active")
        },

        fiClicked() {
            let helsinki = document.querySelector("#helsinki");
            helsinki.classList.toggle("active")
        },

        auClicked() {
            let sidney = document.querySelector("#sidney");
            sidney.classList.toggle("active")
        },
    }
}
</script>

<template>
   <div class="main-container">
    <div class="container-centered">
        <div id="map-container">
            <img src="/public/img/h1-contact-rev-01.png" alt="map">
            <div @click="usClicked()" class="locations" id="US" ><i class="fa-solid fa-plus"></i></div>
            <div @click="fiClicked()" class="locations" id="FI" ><i class="fa-solid fa-plus"></i></div>
            <div @click="auClicked()" class="locations" id="AU" ><i class="fa-solid fa-plus"></i></div>
            
            <div class="locations-info" id="new-york">
                <h2 class="title">New York Coaching</h2>
                <p>READ MORE</p>
            </div>
            <div class="locations-info" id="helsinki">
                <h2 class="title">Helsinki Coaching</h2>
                <p>READ MORE</p>
            </div>    
            <div class="locations-info" id="sidney">
                <h2 class="title">Sidney Coaching</h2>
                <p>READ MORE</p>
            </div>
        </div>

        <div id="form-container">
            <div id="comment">
                <div class="title">
                    <h2>Contact us<span class="orange-dot">.</span></h2>
                </div>
                <div id="description">
                    <p class="grey-text">Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
                </div>
            </div>

            <form class="row g-3" onsubmit="return false">
                <div id="form-up">
                    <div id="form-name">
                        <input type="text" id="name" class="form-control" placeholder="Your Name">
                    </div>
                    <div id="form-email">
                        <input type="email" id="email" class="form-control"  placeholder="Your Email">
                    </div>
                </div>
               
                <div id="form-textarea">
                    <input type="textarea" id="textarea" class="form-control" placeholder="Write a message...">
                </div>

                <button @click="showMessage = true" class=" orange-button">
                    <p>SEND</p>
                    <span>&rightarrow;</span>
                </button>

                <em v-show="showMessage" id="confirm">Thank you! Our staff will receive your request</em>
            </form>
        </div>
    </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 600px;

        align-items: center;
        justify-content: center;

        background-color: #fafafa;

        .container-centered {
            display: flex;
            flex-flow: row;
            align-items: center;
            gap: 50px;

            height: 100%;

            #map-container {
                width: 50%;

                position: relative;

                img {
                    width: 100%;
                }

                .locations {
                    display: flex;
                    align-items: center;
                    justify-content: center;

                    color: white;
                    background-color: #ff4612;

                    width: 25px;
                    height: 25px;

                    border-radius: 50%;
                    text-align: center;

                    position: absolute;
                    cursor: pointer;

                    transition: all .2s ease-in;

                    &#US {
                        top: 100px;
                        left: 130px;
                    }

                    &#FI {
                        top: 60px;
                        left: 280px;
                    }

                    &#AU {
                        bottom: 60px;
                        right: 75px;
                    }

                    &:hover {
                        scale: 1.3;
                    }
                }

                .locations-info {
                    display: flex;
                    flex-flow: column;
                    justify-content: center;

                    background-color: #fff;
                    width: 300px;

                    padding: 20px 30px; 
                    box-shadow: 3px 3px 6px rgba(0, 0, 0, 0.425);

                    position: absolute;
                    display: none;

                    &.active {
                        display: block;
                    }

                    &#new-york {
                        top: 130px;
                        left: 120px;
                    }

                    &#helsinki {
                        top: 90px;
                        left: 270px;
                    }

                    &#sidney {
                        bottom: 30px;
                        right: 105px;
                    }
                }
            }

            #form-container {
                display: flex;
                flex-flow: column;
                justify-content: space-around;
                gap: 20px;

                width: 50%;

                #form-up {
                    display: flex;
                    justify-content: space-between;
                }

                button {
                    font-size: .6em;
                    p {
                        width: 80%;
                        border-right: 0.5px solid;
                    }

                    &:hover p {
                        border-right: 0px;
                    }
                }

                input {
                    border: none;
                    border-bottom: 1px solid rgba(0, 0, 0, 0.226);
                    
                    background-color: transparent;
                    margin-bottom: 20px;

                    padding: 5px;
                    width: 100%;

                    &#name,
                    &#email {
                        width: 250px;
                    }
                    
                    &#textarea {
                        padding-bottom: 80px;
                    }

                }

                #send-message-button button {
                    font-size: .6em;
                }

                #comment {
                    display: flex;
                    flex-flow: column;

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

                        margin-top: 20px;
                }
            }

            #confirm {
                margin-top: 30px;
                color: #ff4612;
            }

            }
        }
    }
</style>

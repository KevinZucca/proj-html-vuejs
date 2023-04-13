<script>

export default {

    data() {
        return {
            name: "AppMain_Section8",

        }
    },
}
</script>

<template>
   <div class="main-container">
    <div class="container-centered">
        <div id="map-container">
            <img src="/public/img/h1-contact-rev-01.png" alt="map">
            <div class="locations" id="US" ><i class="fa-solid fa-plus"></i></div>
            <div class="locations" id="FI" ><i class="fa-solid fa-plus"></i></div>
            <div class="locations" id="AU" ><i class="fa-solid fa-plus"></i></div>
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

            <form class="row g-3">
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

                <button type="submit" class="btn btn-primary orange-button">
                    <p>SEND</p>
                    <span>&rightarrow;</span>
                </button>

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

                #send-message-button {
  
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
            }
        }
    }
</style>

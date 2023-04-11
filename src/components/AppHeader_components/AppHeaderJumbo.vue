<script>
export default {

    data() {
        return {
            name: "AppHeaderJumbo",

        }
    }
}
</script>

<template>
    <div class="main-container">
        <div class="arrow left-arrow">
            <a href="#">&leftarrow;</a>
        </div>
        <div id="intro" class="container">
            <h1>Our Team</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam.</p>
            <div id="buttons-container">
                <button>
                    <p>READ MORE</p>
                    <span>&rightarrow;</span>
                </button>
                <button>
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
        height: 550px;

        justify-content: flex-start;
    
        align-items: center;
        position: relative;

        background-color: rgb(200, 200, 119);

        #intro {
            max-width: 500px;

            margin-left: 180px;

            font-size: 1.5em;
            
            #buttons-container {
                display: flex;
                gap: 15px;

                padding: 20px 30px;

                button {
                    width: 130px;
                    height: 35px;
                    
                    display: flex;
                    align-items: center;
                    justify-content: space-between;

                    cursor: pointer;

                    padding: 8px;

                    span {
                        border-left: 0.5px solid;
                        padding-left: 5px;
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

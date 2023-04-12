<script>

export default {

    data() {
        return {
            name: "FooterContact",

        }
    },
}
</script>

<template>
    <div id="column">
        <div class="title">
            <h2>Contact me</h2>
        </div>
        <div id="description">
            <ul>
                <li>
                    <p class="grey-text">
                       <span><i class="fa-solid fa-location-dot"></i></span>
                       457 BigBlue Street, NY 10013
                    </p>
                </li>
                <li>
                    <p class="grey-text">
                        <span><i class="fa-solid fa-phone"></i></span>
                        (315) 5512-2579
                    </p>
                </li>
                <li>
                    <p class="grey-text">
                        <span><i class="fa-solid fa-envelope"></i></span>
                        everlead@mikado.com
                    </p>
                </li>

                <form  id="form">
                    <div id="form-up">
                        <div id="form-name">
                            <input type="text" id="name" class="form-control" placeholder="Your Name">
                        </div>
                    </div>
                    <button>
                        SUBSCRIBE
                    </button>
                </form>
            </ul>
           
        </div>
    </div>

</template>

<style scoped lang="scss">
  #column {
        display: flex;
        flex-flow: column;

        width: 100%;
        height: 300px;

        .title {
            color: white;
        }

        .title::after {
            content: '';
            height: 2px;
            width: 35px;

            background-color: #ff4612;
            display: block;

            margin: 10px 0
        }

        i {
            width: 26px;
            color: #ff4612;
        }

        ul li {
            margin-bottom: 20px;

            a {
                color: #bdbdbd ;
            }
        }

        #form {
            display: flex;

            border-bottom: 1px solid white;

            input {
                height: 30px;
                background-color: transparent;
                border: none;

                color: white;
            }

            button {
                height: 30px;

                font-size: .8em;
                color: white;
                background-color: transparent;
            }
        }
    }
</style>

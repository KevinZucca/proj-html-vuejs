<script>

export default {

    data() {
        return {
            name: "FooterTwitterItem",

        }
    },
}
</script>

<template>
    <div id="column">
        <div class="title">
            <h2>Twitter</h2>
        </div>
        <div id="description">
            <ul>
                <li>
                    <p class="grey-text">
                       <span><i class="fa-brands fa-twitter"></i></span>
                       <span><a href="#">@aliasadadm</a></span>
                        Hi <span><a href="#">@aliasadadm</a></span> ,
                        can you please submit a ticket at 
                        <span><a href="#">https://tco/JLV61aXG7d</a></span> 
                        and one of our support agent...
                        <span><a href="#">https://tco/yk57k1S9bS</a></span>
                        
                    </p>
                </li>
                <li>
                    <p class="grey-text">
                        <span><i class="fa-brands fa-twitter"></i></span>
                        <span><a href="#">@HenrySefaBoaky1</a></span>
                        Check out our theme Gioia which has all necessary elements to build a multi vendor marketplace.
                        <span><a href="#">https://ico/c9BlYxZBlL</a></span>
                    </p>
                </li>
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
    }
</style>

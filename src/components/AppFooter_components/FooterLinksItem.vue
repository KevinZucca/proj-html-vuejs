<script>

export default {

    data() {
        return {
            name: "FooterLinks",

        }
    },
}
</script>

<template>
    <div id="column">
        <div class="title">
            <h2>Important links</h2>
        </div>
        <div id="description">
            <ul>    
                <li><a href="#">About me</a></li>
                <li><a href="#">About us</a></li>
                <li><a href="#">Language packs</a></li>
                <li><a href="#">Become a coach</a></li>
                <li><a href="#">Monthly events</a></li>
            </ul>
        </div>
    </div>

</template>

<style scoped lang="scss">
  #column {
        display: flex;
        flex-flow: column;

        width: 70%;
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

        ul li a {
            color: #bdbdbd;
            text-decoration: none;
        }
    }
</style>

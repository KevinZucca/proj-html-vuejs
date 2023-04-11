<script>

export default {

    data() {
        return {
            name: "AppMain_Section1",
            cards: [
                {
                    logo: "/public/svg/svg-0.svg",
                    title: "Knowing",
                    subtitle: "lorem ipsum dolor sit amet, quis consect.",
                },
                {
                    logo: "/public/svg/svg-1.svg",
                    title: "Selling",
                    subtitle: "lorem ipsum dolor sit amet, quis consect.",
                },
                {
                    logo: "/public/svg/svg-2.svg",
                    title: "Learning",
                    subtitle: "lorem ipsum dolor sit amet, quis consect.",
                },
                {
                    logo: "/public/svg/svg-3.svg",
                    title: "Contact",
                    subtitle: "lorem ipsum dolor sit amet, quis consect.",
                },
            ]
        }
    },
}
</script>

<template>
   <div class="main-container">
        <div id="title-container">
            <h2>Our specialties<span class="orange-dot">.</span></h2>
            <p class="subtitle">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
        </div>
        <div id="our-mansions">
            <div class="card" v-for="card in cards">
                <div class="logo">
                    <img :src="card.logo" alt="logo">
                </div>
                <div class="title">
                    {{card.title}}
                </div>
                <div class="subtitle">
                    {{card.subtitle}}
                </div>
            </div>
           
        </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        max-width: 95%;
        height: 500px;

        margin: 0 auto;
        background-color: #ffff;

        justify-content: center;
        flex-flow: column;
        text-align: center;

        #title-container {
            margin-bottom: 50px;

            .subtitle::after {
                content: '';
                width: 50px;
                height: 2px;
                background-color: #ff4612;
                display: block;
                
                margin: 10px auto;
            }
        }


        h2 {
            font-size: 3em;
            font-family: serif;
        }


        #our-mansions {
            display: flex;
            gap: 10px;
        }

        .card {
            width: calc(100% / 4);
        }

    }
</style>

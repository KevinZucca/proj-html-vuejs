<script>

export default {

    data() {
        return {
            name: "AppMain_Section3",
            events: [
                {
                    day: "07",
                    monthYear: "Jan 2022",
                    name: "Melbourne Coaching",
                    time: "9:00 am - 5:00 pm, Jan 7, 2022",
                    location: "Cambridge, MA 02138, USA",
                    moreInfo: "READ MORE",
                    img: "public/img/h1-img-07.jpg",
                    index: 0,
                },
                {
                    day: 11,
                    monthYear: "Jan 2022",
                    name: "New York Coaching",
                    time: "9:00 am - 5:00 pm, Jan 11, 2022",
                    location: "Cambridge, MA 02138, USA",
                    moreInfo: "READ MORE",
                    img: "public/img/h1-img-08.jpg",
                    index: 1,
                },
                {
                    day: 21,
                    monthYear: "Jan 2022",
                    name: "London Coaching",
                    time: "9:00 am - 5:00 pm, Jan 21, 2022",
                    location: "Cambridge, MA 02138, USA",
                    moreInfo: "READ MORE",
                    img: "public/img/h1-img-09.jpg",
                    index: 2,
                },
            ],

            mainIndex: 0,

        }
    },

    methods: {
        activateElement(index) {
            let activeElements = document.querySelectorAll(".active");
            activeElements.forEach(element => {
                element.classList.remove("active")
            });
           
            let eventElement = document.querySelectorAll(".event")[index];
             eventElement.classList.add("active")
            this.mainIndex = index;
        },

        backgroundImageUrl() {
            const imageSource = `url(${this.events[this.mainIndex].img})`;
            document.querySelector('.main-container').style.backgroundImage = imageSource;
            return imageSource;
        },

    created() {
        this.mainIndex = this.events[0].index
    },

}


}
</script>

<template>
   <div class="main-container" :style="{ 'background-image': backgroundImageUrl() }">
    <div class="container-centered">
        <div id="events">
            <h3 class="title">Upcoming Events</h3>
            <div @mouseover="activateElement(index)" class="event" v-for="(event,index) in events" :key="index">
                <div class="calendar">
                    <div class="day">
                        {{ event.day }}
                    </div>
                    <div class="month-year">
                        {{ event.monthYear }}
                    </div>
                </div>
                <div class="description">
                    <div class="event-name title">
                         {{ event.name }}
                    </div>
                    <p class="time subtitle">
                        <i class="fa-regular fa-clock"></i>
                        {{ event.time }}
                    </p>
                    <p class="location subtitle">
                        <i class="fa-solid fa-location-dot"></i>
                        {{ event.location }}
                    </p>
                    <strong>
                        {{ event.moreInfo }}
                    </strong>
                </div>
            </div>
        </div>
    </div>
   </div>
</template>

<style scoped lang="scss">
    .main-container {
        width: 100%;
        height: 1000px;

        padding: 0;

        background-image: url("public/img/h1-img-09.jpg");
        background-repeat: no-repeat;

        .container-centered {
            display: flex;
            align-items: center;

            width: 100%;

        #events {
            display: flex;
            flex-flow: column;

            width: 40%;

            background-color: white;

            h3 {
                font-size: 1.5em;
                
                padding: 20px;
                border-bottom: 1px solid rgba(0, 0, 0, 0.237);
                box-shadow: 0 0 7px 0 rgba(0, 0, 0, 0.39);
            }

            .event {
                display: flex;
                flex-flow: row;

                border-bottom: 1px solid rgba(0, 0, 0, 0.237);
                padding: 20px;

                cursor: pointer;

                &.active {
                    background-color: #fafafa;

                    .title {
                        color: #ff4612;
                    }
                }

                .event-name {
                    font-size: 1.3em;
                }

                i {
                    color: #ff4612;
                }

                .calendar {
                    display: flex;
                    flex-flow: column;

                    background-color: #ff4612;
                    color: white;

                    text-align: center;
                    height: 50px;
                    width: 70px;

                    padding: 8px;
                    margin-right: 20px;
                    margin-top: 10px;
                    font-size: .8em;
                }

                .description {
                    display: flex;
                    flex-flow: column;
                }
            }
        }
    }


 }
</style>

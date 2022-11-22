<script>
import icons from '../data/icon.js'
export default {
    name: 'MainFirst',
    data() {
        return {
            icons: icons
        }
    }
}

</script>

<template>
    <section>
        <!-- //Container Delle icone per info -->
        <div class="infobar">
            <!-- //Container layout icone -->
            <div class="infoContainer">
                <div v-for="(icon, index) in icons" :key="index" class="icons">
                    <img :src="(`/icone/${icon.img}`)" alt="">
                    <h3> {{ icon.text }} </h3>
                </div>
                <!-- <div class="icons">
                    <img src="../assets/img/h5-custom-icon-1.png" alt="">
                    <h3> Languages </h3>
                </div>
                <div class="icons">
                    <img src="../assets/img/h5-custom-icon-2.png" alt="">
                    <h3> Software </h3>
                </div>
                <div class="icons">
                    <img src="../assets/img/h5-custom-icon-3.png" alt="">
                    <h3> Business </h3>
                </div>
                <div class="icons">
                    <img src="../assets/img/h5-custom-icon-4.png" alt="">
                    <h3> Chemistry </h3>
                </div>
                <div class="icons">
                    <img src="../assets/img/h5-custom-icon-5.png" alt="">
                    <h3> Science </h3>
                </div>
                <div class="icons">
                    <img src="../assets/img/h5-custom-icon-6.png" alt="">
                    <h3> DIY&Craft </h3>
                </div> -->
            </div>
            <!-- ***/Container layout icone -->
        </div>
        <!-- ***/Container Delle icone per info -->

        <!-- //Sezione testo  -->
        <div class="sectionText">
            <h1>The Trusted Name <br> for In-Home Tutoring.</h1>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officiis autem, eveniet omnis fugiat alias
                excepturi, magni doloremque similique fuga quae rerum minus voluptatibus, et minima tempore laudantium
                optio temporibus voluptas?</p>
            <p class="moreInfo">Learn MORE</p>
        </div>
        <!-- ***/Sezione testo  -->

        <!-- //jumbotron image -->
        <div class="jumbotron">
            <img src="../assets/img/h5-img-1.jpg" alt="">
            <div class="top1">
                <i class="fas fa-angle-up"></i>
                top
            </div>
        </div>
        <!-- ***/jumbotron image  -->

        <!-- //Sezione mappa mondo e scritta a destra  -->
        <div class="worldSection">
            <!-- //TOP laterale -->
            <div class="top2">
                <i class="fas fa-angle-up"></i>
                top
            </div>
            <!-- ***/TOP laterale -->

            <!-- //Container sezione -->
            <div class="small">
                <!-- //Parte sinistra  -->
                <div class="worldMap">
                    <img src="../assets/img/h5-img-2.jpg" alt="">
                </div>
                <!-- ***/Parte sinistra  -->
                <!-- //Parte destra -->
                <div class="big">
                    <!-- //Titolo -->
                    <h1 class="bigTitle">
                        Empowering <br> Children to Reach <br> Their Potential
                    </h1>
                    <!-- ***/Titolo -->
                    <p class="lorem">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quos accusamus, alias
                        rerum expedita commodi illum consequuntur? Sapiente consectetur vitae repellendus facere dolorem
                        mollitia suscipit quae ducimus, quasi ab veritatis officia!</p>
                    <!-- //Parte numeri -->
                    <div class="number">
                        <div>
                            <p class="user">168</p>
                            <p class="userText"> User Stories</p>
                        </div>
                        <div>
                            <p class="event">347</p>
                            <p class="eventText">Events</p>
                        </div>
                    </div>
                    <!-- ***/Parte numeri -->
                </div>
                <!-- ***/Parte destra -->
            </div>
            <!-- ***/Container sezione -->
        </div>
        <!-- ***/Sezione mappa mondo e scritta a destra  -->
    </section>

</template>

<style lang="scss" scoped>
.infobar {
    width: 100%;
    height: 300px;
    margin-top: 50px;

    .infoContainer {
        width: 95%;
        height: 300px;
        margin: 0 auto;
        display: flex;
        justify-content: center;
        align-items: center;
        justify-content: space-between;

        .icons {
            width: calc(1200px / 6);
            margin: 3px;
            height: 250px;
            background: #F2F8FC;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            &:hover {
                transform: scale(1.3);
                transition: 2s;
                cursor: pointer;
            }

            h3 {
                margin-top: 15px;
            }
        }
    }

}

.sectionText {
    width: 95%;
    margin: 50px auto;

    h1 {
        font-size: 50px;
    }

    p {
        margin-top: 25px;
        color: #5c5b5b;
        font-size: 22px;
    }

    .moreInfo {
        width: 95%;
        margin-top: 25px;
        text-transform: uppercase;
        color: #40C4FE;
        font-size: 18px;
    }
}



.jumbotron {
    width: 95%;
    width: 100%;
    text-align: center;
    margin: 0 auto;
    position: relative;

    &>img {
        width: 100%;
    }

    .top1 {
        bottom: 30%;
        right: 0;
        transform: translate(0%, -50%);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: absolute;
        width: 50px;
        height: 50px;
        color: white;
        background-color: #40C4FE;
        text-transform: uppercase;
    }
}

.worldSection {
    margin: 50px auto;
    width: 100%;
    position: relative;

    .top2 {
        bottom: 0%;
        right: 0;
        transform: translate(0%, -50%);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: absolute;
        width: 50px;
        height: 50px;
        color: white;
        background-color: #40C4FE;
        text-transform: uppercase;

    }

    .small {
        margin: 50px auto;
        display: flex;
        justify-content: center;
        width: 90%;
        margin: 0 auto;

        .worldMap {
            width: 50%;
            display: flex;
            align-items: flex-end;
            justify-content: center;

            &>img {
                width: 100%;
            }
        }

        .big {
            width: 50%;
            padding: 30px;

            .bigTitle {
                font-size: 50px;
            }

            .lorem {
                margin: 40px auto;
            }

            .number {
                display: flex;

                .user,
                .event {
                    font-size: 60px;
                    font-weight: bold;
                    color: #40C4FE;
                }

                .userText,
                .eventText {
                    margin-top: 0px;
                    color: #40C4FE;
                }

                .user {
                    margin-right: 150px;
                }
            }
        }
    }
}
</style>



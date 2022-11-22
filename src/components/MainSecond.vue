<script>
export default {
    name: 'MainSecond',
    data() {
        return {
            informations: [
                {
                    titolo: "What We Do",
                    status: true
                },
                {
                    titolo: "Degree Programme",
                    status: false
                },
                {
                    titolo: "Career Achievements",
                    status: false
                },
                {
                    titolo: "Personal Managment",
                    status: false
                },
                {
                    titolo: "Steps To Success",
                    status: false
                },
                {
                    titolo: "Knowledge Transfer",
                    status: false
                },
            ],
            objectives: [
                {
                    titolo: "We enrich lives through learning.",
                },
                {
                    titolo: "Maximizing potential through individual attention.",
                },
                {
                    titolo: "The trusted name for specialized training.",
                },
                {
                    titolo: "People thach. People learn. This is where they connect.",
                },
            ]
        }
    }
}
</script>


<template>
    <section>
        <!-- //Jumbo  -->
        <div class="jumbotron">
            <!-- Logo top a lato  -->
            <div class="top">
                <i class="fas fa-angle-up"></i>
                top
            </div>
            <!-- ***/Logo top a lato  -->
            <!-- //Container immagine testimonial -->
            <div class="testimonial">
                <img src="../assets/img/testimonials-standard-2.png" alt="">
            </div>
            <!-- ***/Container immagine testimonial -->
            <!-- //Container paragrafo -->
            <div class="para">
                <p>"Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, eum praesentium aliquam
                    molestias voluptas deleniti, suscipit, maxime quo nostrum natus rem cum voluptatum repellat eligendi
                    vero cumque. Harum, inventore ex! aliquam molestias voluptas deleniti"</p>
            </div>
            <!-- ***/Container paragrafo -->
            <div class="id">Joan Collins</div>
            <div class="position">STUDENT</div>
            <!-- //Cerchi parte inferiore -->
            <div class="headerBottom">
                <div v-for="n in 3" :key="n" class="cerchio">
                    {{ n.cerchio }}
                    <div class="inner"></div>
                </div>
            </div>
            <!-- ***/Cerchi parte inferiore -->
        </div>
        <!-- ***/Jumbo  -->
        <!-- //Container sezione Info -->
        <div class="info">
            <!-- //Griglia info sinistra dinamica -->
            <div class="leftInfo">
                <div v-for="(info, index) in informations" :key="index" class="voices">
                    <div :class="(info.status) ? 'active, test' : null"></div>
                    <p class="blueBar">{{ info.titolo }}</p>
                </div>
            </div>
            <!-- ***/Griglia info sinistra dinamica -->
            <!-- //Info parte destra -->
            <div class="rightInfo">
                <!-- //Container testo statico e lista dinamica -->
                <div class="titolo">
                    <h1 class="learning">Learning Possibilities</h1>
                    <p class="lorem">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex accusamus excepturi
                        consequatur vel, amet optio temporibus nobis reiciendis? Laudantium quaerat tempora, id natus
                        quasi possimus esse rem molestias ullam minima.
                        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Autem consequatur odit repellat
                        accusantium iste modi. Adipisci facere doloremque aliquam debitis magni? Neque ullam molestias
                        mollitia ducimus deserunt eligendi assumenda porro!
                    </p>
                    <!-- //Lista dinamica -->
                    <ul class="lista">
                        <li v-for="(objective, index) in objectives" :key="index" class="nav">
                            <i class="fas fa-check"></i>
                            {{ objective.titolo }}
                        </li>
                    </ul>
                    <!-- ***/Lista dinamica -->
                    <!-- //Immagine figura geometrica -->
                    <div class="square">
                        <img src="../assets/img/h12-tabs-icon-1.png" alt="">
                    </div>
                    <!-- ***/Immagine figura geometrica -->
                </div>
                <!-- ***/Container testo statico e lista dinamica -->
            </div>
            <!-- ***/Info parte destra -->
        </div>
        <!-- ***/Container sezione Info -->
    </section>

</template>



<style lang="scss" scoped>
.jumbotron {
    height: 800px;
    width: 100%;
    background-image: url('../assets/img/h5-parallax-img-1.png');
    background-repeat: no-repeat;
    background-size: 200%;
    background-position: top, bottom;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .top {
        right: 0;
        top: 103%;
        position: absolute;
        width: 50px;
        height: 50px;
        color: white;
        background-color: #40C4FE;
        text-transform: uppercase;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .testimonial {
        width: 100px;
        height: 100px;

        &>img {
            width: 100%;
            border-radius: 50%;
        }
    }

    .para {
        width: 50%;
        margin: 80px auto;
        text-align: center;
        color: white;
        font-size: 22px;
    }

    .id {
        margin-bottom: 20px;
        color: white;
        font-size: 25px;
    }

    .position {
        color: white;
    }

    .headerBottom {
        width: 100%;
        height: 50px;
        margin-top: 30px;
        display: flex;
        justify-content: center;
        align-items: center;

        .cerchio {
            margin: 0 5px;
            background: white;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;


        }

    }

}

.info {
    width: 95%;
    height: 700px;
    margin: 100px auto;
    display: flex;

    .leftInfo {
        width: 20%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        .voices {
            width: 100%;
            height: 100px;
            border: 1px solid #EAEAEA;
            display: flex;
            align-items: center;

            :hover,
            .active {
                color: #40C4FE;
                border-left: 10px solid #40C4FE;
                height: 100%;
                padding-left: 20px;
                display: flex;
                align-items: center;
            }

            .blueBar {
                padding-left: 30px;
                font-weight: bold;
                color: #5c5b5b;
                font-size: 22px;

                &:hover {
                    cursor: pointer;
                }
            }
        }
    }

    .rightInfo {
        width: 80%;
        height: 100%;
        display: flex;
        align-items: center;

        .titolo {
            position: relative;
            width: 80%;
            height: 90%;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            justify-content: space-around;

            .learning {
                font-size: 50px;
            }

            .lorem {
                margin-top: 40px;
                color: #5c5b5b;
                font-size: 22px;
            }

            .lista {
                margin-top: 50px;

                .nav {
                    margin: 25px 0;
                    list-style: none;
                    color: #A8A1A2;
                    font-size: 22px;

                    .fa-check {
                        color: #40C4FE;
                        font-size: 15px;
                    }
                }
            }

            .square {
                position: absolute;
                bottom: 0px;
                right: 0px;
            }
        }
    }
}
</style>
<script>

import cards from '../data/card.js'
export default {
    name: 'MainThird',
    data() {
        return {
            cards: cards,
        }
    }
}

</script>


<template>
    <section>
        <div class="bigContainer">
            <div class="background"></div>
            <div class="smallContainer">
                <div class="text">
                    <h1>Popular Online Courses</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat repellat libero molestiae
                        obcaecati consequuntur laborum voluptatum, similique ipsum! Rerum ut facilis quis mollitia quasi
                        facere illum dignissimos saepe dolorum fuga?</p>
                </div>
                <div class="cardsContainer">
                    <div v-for="(card, index) in cards" :key="index" class="card">
                        <div class="cardImg">
                            <img :src="(`/icone/${card.img}`)" alt="">
                        </div>
                        <div class="cardDescription">
                            <div class="cardInfo">
                                <h3> {{ card.professione }} </h3>
                                <div :class="(card.status) ? 'active' : null" class="price">
                                    {{ card.prezzo }}
                                </div>

                            </div>
                            <p class="nome"> {{ card.nome }} </p>
                            <p class="paragrafo"> {{ card.paragrafo }} </p>
                            <p class="paragrafo"> sostituire </p>
                        </div>
                        <div class="icone"></div>
                    </div>
                </div>
                <div class="bottom">
                    <div v-for="n in 3" :key="n" class="cerchio">
                        {{ n.cerchio }}
                        <div class="inner"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>



<style lang="scss" scoped>
.bigContainer {
    position: relative;
    width: 100%;
    height: 1000px;
    border-top: 1px solid grey;
    border-bottom: 1px solid grey;
    padding: 10px;
    display: flex;
    align-items: center;
    flex-direction: column;

    .background {
        background-image: url('../assets/img/page-background-img.png');

        background-size: 190%;
        background-position: 0px -15px;
        transform: rotate(-180deg);
        width: 100%;
        height: 100%;
    }

    .smallContainer {
        position: absolute;
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        .text {
            width: 70%;
            margin: 50px auto;
            text-align: center;

            h1 {
                margin-bottom: 20px;
                font-size: 60px;
            }

            p {
                margin-bottom: 22px;
                font-size: 20px
            }
        }

        .cardsContainer {
            width: 95%;
            height: 500px;
            margin: 0 auto;
            display: flex;
            align-items: center;

            .card {
                width: calc(100% / 3);
                height: 450px;
                margin: 0px 5px;

                .cardImg {
                    width: 100%;
                    height: 200px;

                    &>img {
                        object-fit: cover;
                        width: 100%;
                        height: 100%;
                    }
                }

                .cardDescription {
                    padding: 15px;
                    height: 250px;
                    border: 1px solid rgb(206, 206, 206);

                    .cardInfo {
                        display: flex;
                        align-items: center;
                        justify-content: space-between;

                        .active {
                            height: 100%;
                            background: #FFD740;
                        }

                        .price {
                            width: 50px;
                            height: 100%;
                            border-radius: 20px;
                            padding: 2px;
                            background: #40C4FE;
                            color: white;
                            text-transform: uppercase;
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            font-size: 13px;
                        }

                    }


                    .paragrafo {
                        font-size: 18px;
                    }

                    .nome {
                        margin-top: 5px;
                        font-size: 15px;
                    }
                }

            }
        }


        .bottom {
            width: 50%;
            height: 30px;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            align-items: center;

            .cerchio {
                margin: 0 5px;
                background: #40C4FE;
                width: 15px;
                height: 15px;
                border-radius: 50%;
            }
        }
    }
}
</style>

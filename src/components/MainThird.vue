<script>
import cards from '../data/card.js'
import packages from '../data/packages.js'
import courses from '../data/courses.js'
import colSx from '../data/colSx.js'
import colCx from '../data/colCx.js'
import colDx from '../data/colDx.js'
import studies from '../data/studies.js'

export default {
    name: 'MainThird',
    data() {
        return {
            cards: cards,
            packages: packages,
            courses: courses,
            colSx: colSx,
            colCx: colCx,
            colDx: colDx,
            studies: studies
        }
    }
}
</script>


<template>
    <section>
        <!-- //Container section -->
        <div class="container">
            <div class="background"></div>
            <div class="top">
                <i class="fas fa-angle-up"></i>
                top
            </div>
            <div class="top-special">
                <i class="fas fa-angle-up"></i>
                top
            </div>
            <div class="top-special-due">
                <i class="fas fa-angle-up"></i>
                top
            </div>
            <div class="top-special-logo">
                <img src="../assets/img/cerchio.png" alt="">
            </div>
            <div class="top-special-shopping">
                <i class="fas fa-shopping-cart"></i>
            </div>
            <div class="top-special-due">
                <i class="fas fa-angle-up"></i>
                top
            </div>
            <div class="containerBig">
                <div class="textContainer">
                    <h1>Popular Online Courses</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat repellat libero molestiae
                        obcaecati consequuntur laborum voluptatum, similique ipsum! Rerum ut facilis quis mollitia quasi
                        facere illum dignissimos saepe dolorum fuga?</p>
                </div>
                <div class="cardContainer">
                    <div v-for="(card, index) in cards" :key="index" class="card">
                        <div class="cardImg">
                            <img :src="(`/icone/${card.img}`)" alt="">
                        </div>
                        <div class="cardDescription">
                            <div class="cardInfo">
                                <h3 class="professione"> {{ card.professione }} </h3>
                                <div :class="(card.status) ? 'active' : null" class="prezzo">
                                    {{ card.prezzo }}
                                </div>

                            </div>
                            <p class="nome"> {{ card.nome }} </p>
                            <p class="paragrafo"> {{ card.paragrafo }} </p>
                            <p class="paragrafo"><i class="fas fa-user"></i> 1 <i class="fas fa-tag"></i> Programming
                            </p>

                        </div>

                    </div>
                </div>
                <div class="containerCircles">
                    <div v-for="n in 3" :key="n" class="cerchio">
                        {{ n.cerchio }}
                    </div>
                </div>
                <div class="containerBig2">
                    <div class="textContainer2">
                        <h1>Pricing Plans</h1>
                        <p>Quaerat repellat libero molestiae obcaecati consequuntur laborum voluptatum, similique ipsum!
                        </p>
                    </div>
                    <div class="cardContainer2">
                        <div class="left">
                            <div class="boxTop">
                                <p class="save">Save up to 40% by paying weekly</p>
                            </div>
                            <div class="boxCells">
                                <div v-for="(course, index) in courses" :key="index" class="cell">
                                    <p class="titolo">{{ course.titolo }}</p>
                                </div>
                            </div>
                        </div>
                        <div class="right">
                            <div class="boxTop2">
                                <div v-for="(pack, index) in packages" :key="index" class="package">
                                    <img :src="(`/icone/${pack.img}`)" alt="">
                                    <h3 class="piano"> {{ pack.piano }} </h3>
                                    <p class="price"> {{ pack.price }} </p>
                                </div>
                            </div>
                            <div class="containerBox">
                                <div class="boxContainer">
                                    <div v-for="(col, index) in colSx" :key="index" class="righe">
                                        <p class="testi">
                                            {{ col.titolo }}
                                            <i :class="(col.current) ? 'fas fa-check' : 'fas fa-times'"></i>
                                        </p>

                                    </div>
                                    <div class="getRows">
                                        <p class="textRows">GET IT NOW</p>
                                    </div>
                                </div>
                                <div class="boxContainer">
                                    <div v-for="(col, index) in colCx" :key="index" class="righe">
                                        <p class="testi">
                                            {{ col.titolo }}
                                            <i :class="(col.current) ? 'fas fa-check' : 'fas fa-times'"></i>
                                        </p>
                                    </div>
                                    <div class="getRows">
                                        <p class="textRows">GET IT NOW</p>
                                    </div>
                                </div>
                                <div class="boxContainer">
                                    <div v-for="(col, index) in colDx" :key="index" class="righe">
                                        <p class="testi">
                                            {{ col.titolo }}
                                            <i :class="(col.current) ? 'fas fa-check' : 'fas fa-times'"></i>
                                        </p>

                                    </div>
                                    <div class="getRows">
                                        <p class="textRows">GET IT NOW</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- ***/Container section -->
        <!-- //Container loghi bottom -->
        <div class="containerLoghi">
            <!-- //TOP LOGO  -->
            <div class="top-loghi">
                <i class="fas fa-angle-up"></i>
                top
            </div>
            <!-- ***/TOP LOGO  -->
            <!-- //Loghi aziende modo dinamico -->
            <div class="logotipi">
                <div v-for="(study, index) in studies" :key="index" class="loghi">
                    <img :src="(`/icone/${study.img}`)" alt="">
                </div>
            </div>
            <!-- ***/Loghi aziende modo dinamico -->
        </div>
        <!-- ***/Container loghi bottom -->
    </section>

</template>



<style lang="scss" scoped>
.fa-check {
    color: #40C4FE;
}

.fa-times {}

.top {
    right: 0;
    top: 0;
    transform: translate(0, 50%);
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

.top-special {
    position: absolute;
    width: 50px;
    height: 50px;
    color: white;
    background-color: #40C4FE;
    text-transform: uppercase;
    top: 780px;
    right: 0;
    z-index: 10;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.top-special-due {
    position: absolute;
    width: 50px;
    height: 50px;
    color: white;
    background-color: #40C4FE;
    text-transform: uppercase;
    top: 1500px;
    right: 0;
    z-index: 10;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.top-loghi {
    position: absolute;
    width: 50px;
    height: 50px;
    color: white;
    background-color: #40C4FE;
    text-transform: uppercase;
    top: 0;
    right: 0;
    z-index: 10;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.top-special-logo {
    position: absolute;
    width: 40px;
    height: 40px;
    color: white;
    background-color: #EE2852;
    text-transform: uppercase;
    top: 1350px;
    right: 0;
    z-index: 10;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.top-special-logo>img {
    width: 100%;
}

.top-special-shopping {
    position: absolute;
    width: 40px;
    height: 40px;
    color: #EE2852;
    background-color: white;
    text-transform: uppercase;
    top: 1400px;
    right: 0;
    z-index: 10;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.container {
    position: relative;
    width: 100%;
    height: 2300px;
    border-top: 1px solid grey;
    border-bottom: 1px solid grey;
    display: flex;
    align-items: center;
    flex-direction: column;
}

.background {
    background-image: url('../assets/img/page-background-img.png');
    width: 100%;
    height: 100%;
}

.containerBig {
    position: absolute;
    top: 0px;
    padding-top: 100px;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.textContainer {
    width: 70%;
    margin: 50px auto;
    text-align: center;
}

h1 {
    margin-bottom: 20px;
    font-size: 60px;
}

p {
    margin-bottom: 22px;
    font-size: 20px;
}

.cardContainer {
    width: 95%;
    height: 500px;
    margin: 0px auto;
    display: flex;
    align-items: center;
}

.card {
    width: calc(100% / 3);
    height: 450px;
    margin: 0px 5px;

    &:hover {
        transform: scale(0.9);
        transition: 2s;
        cursor: pointer;
    }
}

.cardImg {
    width: 100%;
    height: 200px;
}

.cardImg>img {
    object-fit: cover;
    width: 100%;
    height: 100%;
}

.cardDescription {
    padding: 15px;
    height: 250px;
    border: 1px solid rgb(206, 206, 206);

}

.cardInfo {
    display: flex;
    align-items: center;
    justify-content: space-between;

    .active {
        height: 100%;
        background: #FFD740;
    }
}

.professione {
    font-weight: bold;
    color: #3E3E3E;
}

.nome {
    margin-top: 5px;
    color: #CECECE;
    font-size: 15px;
}

.paragrafo {
    margin-bottom: 20px;
    color: #5c5b5b;
    font-size: 18px;
}

.prezzo {
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

.containerCircles {
    width: 50%;
    height: 30px;
    margin: 30px auto;
    display: flex;
    justify-content: center;
    align-items: center;
}

.cerchio {
    margin: 0 5px;
    background: #40C4FE;
    width: 15px;
    height: 15px;
    border-radius: 50%;
}

.containerBig2 {
    margin: 30px 0px;
    padding: 100px 0px;
    border-top: 1px solid grey;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.textContainer2 {
    width: 70%;
    margin: 50px auto;
    text-align: center;
}

.cardContainer2 {
    width: 95%;
    height: 100%;
    margin: 0 auto;
    display: flex;
}

.left {
    width: 30%;
}

.right {
    position: relative;
    width: 70%;
}

.boxTop {
    position: relative;
    width: 100%;
    height: 300px;
    border: 1px solid #EAEAEA;
    border-top: 5px solid #D6F2FF;
}

.save {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%);
    font-size: 30px;
    font-weight: bold;
    color: #3E3E3E;
    font-size: 25px;
}

.price {
    margin: 30px;
    font-weight: bold;
    color: #3E3E3E;
    font-size: 25px;
}

.sottoColonna {
    font-weight: bold;
    color: #545454;
}

.boxCells {
    width: 100%;
    height: calc(100% - 300px);
}

.cell {
    position: relative;
    width: 100%;
    height: calc(100% / 8);
    border: 1px solid #EAEAEA;
    color: #5c5b5b;
    font-weight: bold;
}

.titolo {
    position: absolute;
    top: 50%;
    left: 25%;
    transform: translate(0%, -50%);
}

.boxTop2 {
    width: 100%;
    height: 275px;
    display: flex;
    background: #F2F8FC;
}

.package {
    width: calc(100% / 3);
    height: 275px;
    border: 1px solid #EAEAEA;
    border-top: 5px solid #D6F2FF;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    &:hover {
        cursor: pointer;
        border-top: 5px solid #40C4FE;
    }
}

.containerBox {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: calc(100% - 275px);
    display: flex;
}

.boxContainer {
    width: calc(100% / 3);
    height: calc(100% - 50px);
}

.righe {
    width: calc(100%);
    height: calc(100% / 8);
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid #EAEAEA;
    color: #5c5b5b;
}

.testi {
    margin: 50% auto;
}

.getRows {
    width: 100%;
    height: 90px;
    border: 1px solid #EAEAEA;
    background: #F2F8FC;
    display: flex;
    justify-content: center;
    align-items: center;
}

.textRows {
    margin: 50% auto;
    width: 60%;
    height: 70%;
    border: 1px solid #EAEAEA;
    text-transform: uppercase;
    color: #5c5b5b;
    background: white;
    display: flex;
    justify-content: center;
    align-items: center;

    &:hover {
        cursor: pointer;
        background-color: #40C4FE;
        transform: scale(1.1);
        transition: 2s;
        color: white;
    }
}

.containerLoghi {
    width: 100%;
    height: 300px;
    position: relative;
}

.logotipi {
    margin: 0 auto;
    width: 95%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.loghi {
    width: 100%;
    margin: 0 auto;
    cursor: pointer;

    &:hover {
        transform: scale(1.2);
        transition: 2s;
    }
}

.loghi>img {
    width: 100%;
}
</style>
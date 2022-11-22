<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            linkSx: [
                {
                    text: "Providing Life Changing",
                    textUno: "Experiences Through",
                    textDue: "Education Class That Fit your",
                    textTre: "Busy life. closer to home",
                    url: "#",
                },
                {
                    text: "1-677-124-44227",
                    url: "#",
                },
                {
                    text: "mon - sat 8.00 - 18:00",
                    url: "#",
                },
            ],
            linkCx: [
                {
                    text: "Business english",
                    name: "Preston marshall",
                    url: "#",
                },
                {
                    text: "social computing",
                    name: "david sanders",
                    url: "#",
                },
                {
                    text: "learn spanish",
                    name: "jennie king",
                    url: "#",
                },
            ],
            linkDx: [
                {
                    text: "User dashboard",
                    url: "#",
                },
                {
                    text: "Contact Us",
                    url: "#",
                },
                {
                    text: "FAQ",
                    url: "#",
                },
                {
                    text: "Course Offer",
                    url: "#",
                },
                {
                    text: "Events",
                    url: "#",
                },
            ]
        }
    }
}

</script>


<template>
    <footer>
        <div class="backgroundFooter">
            <div class="top-footer">
                <i class="fas fa-angle-up"></i>
                top
            </div>
            <div class="link">
                <div class="academy">
                    <img src="../img/logo-light.png" alt="">
                    <ul>
                        <li v-for="(link, index) in linkSx" :key="index">
                            <p> {{ link.text }} </p>
                            <p> {{ link.textUno }} </p>
                            <p> {{ link.textDue }} </p>
                            <p> {{ link.textTre }} </p>
                        </li>
                    </ul>
                </div>
                <div class="courses">
                    <h1>Popular courses</h1>
                    <ul>
                        <li v-for="(link, index) in linkCx" :key="index">
                            <p> {{ link.text }} </p>
                            <p> {{ link.name }} </p>
                        </li>
                    </ul>
                </div>
                <div class="support">
                    <h1>Support</h1>
                    <ul>
                        <li v-for="(link, index) in linkDx" :key="index">
                            {{ link.text }}
                        </li>
                    </ul>
                </div>
                <div class="learning">
                    <h1>Flexible Learning</h1>
                    <img src="../assets/img/footer-img-1.png" alt="">
                </div>
            </div>
            <div class="footerBottom">
                <div class="copy">
                    <p>Copyrights 2017 ©Mikado Themes</p>
                </div>
                <div class="socials">
                    <p>CALL +44 300 303 0266</p>
                    <p class="follow">FOLLOW US</p>
                    <div class="icons">
                        <i class="fab fa-twitter"></i>
                        <i class="fab fa-instagram"></i>
                        <i class="fab fa-facebook-f"></i>
                    </div>
                </div>
            </div>
        </div>
    </footer>

</template>

<style scoped lang="scss">
.backgroundFooter {
    position: relative;
    width: 100%;
    height: 500px;
    background: #222222;
    display: flex;
    align-items: center;
    overflow-x: hidden;

    .top-footer {
        right: 0;
        bottom: 0;
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

    .link {
        width: 95%;
        height: 300px;
        margin: 0 auto;
        display: flex;
        justify-content: center;
        align-items: center;
        justify-content: space-between;
        border-bottom: 1px solid #ABABAB;

    }

    .academy,
    .courses,
    .support,
    .learning {
        width: 20%;
        height: 100%;
        margin: 10px;

        .academy>img {
            width: 150px;
            margin-bottom: 20px;
        }

        .learning>img {
            width: 100%;
        }

        h1 {
            margin-bottom: 20px;
            color: white;
        }

        ul,
        li {
            list-style: none;
            margin-bottom: 20px;
            color: #ABABAB;

            &:hover {
                color: #40C4FE;
                transform: scale(1.1);
                transition: 2s;
                cursor: pointer;
            }
        }

        p {
            margin: 10px 0px;
        }

    }
}


.footerBottom {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translate(-50%, 0%);
    width: 95%;
    height: 100px;
    display: flex;
    color: #ABABAB;

    .copy {
        width: 50%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: left;
    }

    .socials {
        width: 50%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: right;
        cursor: pointer;


        .follow {
            margin: 0 20px;
        }

        .icons {
            margin-right: 10px;

            .fab {
                font-size: 20px;
                margin: 0px 20px;
            }
        }
    }
}
</style>

<script>
export default {
    name: "AppHeader",

    data() {
        return {
            links: [
                {
                    text: "Home",
                    url: "#",
                },
                {
                    text: "Courses",
                    url: "#",
                },
                {
                    text: "Istructor",
                    url: "#",
                },
                {
                    text: "Events",
                    url: "#",
                },
                {
                    text: "Pages",
                    url: "#",
                },
                {
                    text: "Elements",
                    url: "#",
                },
            ]
        }
    }
}
</script>

<template>
    <div class="headerBack">
        <div class="layer"></div>
        <div class="headerTop">
            <div class="logo">
                <img src="../assets/img/footer-logo-1.png" alt="">
            </div>
            <nav class="navigazione">
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a> {{ link.text }} </a>
                    </li>
                </ul>
            </nav>
            <div class="icone">
                <i class="fas fa-search"></i>
                <i class="far fa-clipboard">
                    <div class="cart"> 0 </div>
                </i>
                <!-- <div class="qnt">0</div> -->
                <i class="fas fa-bars"></i>
            </div>
        </div>
        <div class="headerCenter">
            <h1>Contemporary Ideas</h1>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                Eligendi quis natus totam veniam, commodi dolorum inventore,
                deleniti quasi laborum obcaecati blanditiis libero voluptatem error aut
                repudiandae facilis architecto ex? Blanditiis?</p>
            <div class="register">
                <!-- <div> -->
                <p class="now"><a href=""> Register Now</a></p>
                <!-- </div> -->
            </div>
        </div>
        <div class="headerBottom">
            <div v-for="n in 3" :key="n" class="circles">
                {{ n.cerchio }}
                <div class="innercircle"></div>
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
.headerBack {
    position: relative;
    width: 100%;
    height: 900px;
    background-image: url('../assets/img/course-9-f-img.jpg');
    background-repeat: no-repeat;
    background-size: cover;

    .layer {
        position: absolute;
        width: 100%;
        height: 100%;
        background: rgb(6, 6, 6, 0.3);
    }

    .headerTop {
        position: absolute;
        left: 50%;
        transform: translate(-50%);
        width: 95%;
        height: 100px;
        margin: 0px auto;
        display: flex;
        justify-content: center;
        align-items: center;
        justify-content: space-between;
        width: 90%;
        margin: 0 auto;

        .logo {
            text-align: start;
            width: 200px;
            display: flex;
            align-items: center;

            &>img {
                width: 100%;
            }
        }

        ul,
        li {
            width: 100%;
            display: flex;
            list-style: none;
            margin: 20px;
            text-transform: uppercase;
            color: white;
        }

        .icone {
            text-align: end;
            width: 200px;

            .fas {
                margin-right: 20px;
                font-size: 20px;
                color: white;
            }


            .fa-clipboard {
                position: relative;
                margin-right: 20px;
                font-size: 20px;
                color: white;
            }

            .cart {
                position: absolute;
                top: 0;
                right: 0;
                transform: translate(60%, -20%);
                width: 15px;
                height: 15px;
                border-radius: 50%;
                background: #40C4FE;
                font-size: 12px;
                display: flex;
                justify-content: center;
                align-items: center;
            }


        }

    }

    .headerCenter {
        position: absolute;
        width: 80%;
        margin: 0 auto;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;

        h1 {
            font-size: 90px;
            margin-bottom: 30px;
            color: white;
        }

        p {
            margin-bottom: 30px;
            color: white;
            font-size: 20px;

            a {
                text-decoration: none;
                color: white;
            }
        }

        .register {
            position: relative;
            width: 200px;
            height: 70px;
            margin: 0px auto;
            text-transform: uppercase;
            background: #40C4FE;
            color: white;


            &:hover {
                transform: scale(1.2);
                transition: 2s;
            }

            .now {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                width: 80%;
                font-size: 18px;
            }
        }
    }

    .headerBottom {
        position: absolute;
        bottom: 0;
        width: 100%;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;

        .circles {
            width: 20px;
            height: 20px;
            margin: 0 5px;
            border-radius: 50%;
            border: 2px solid white;
            display: flex;
            justify-content: center;
            align-items: center;

            .innercircle {
                width: 10px;
                height: 10px;
                border-radius: 50%;
                background: white;
            }
        }
    }

}
</style>
<script>
export default {
    name: "MainComponent",
    data() {
        return {
            cardsNewCourses: [
                {
                    cardImage: "../src/assets/img/electronic.jpeg",
                    cardTitle: "How to be a DJ? Make Electronic Music",
                    cardParagraph: "Electronic",
                    cardDifficult: "Advanced",
                    cardDuration: "8 lectures",
                    cardHours: "6 hours",
                    cardButton: true,
                    cardPrice: "$59" 
                },
                {
                    cardImage: "../src/assets/img/nvidia.png",
                    cardTitle: "Nvidia and UE4 Technologies Practice",
                    cardParagraph: "Nvidia",
                    cardDifficult: "Advanced",
                    cardDuration: "8 lectures",
                    cardHours: "6 hours",
                    cardButton: true,
                    cardPrice: "$60"
                },
                {
                    cardImage: "../src/assets/img/fashion.jpeg",
                    cardTitle: "Fashion Photography from professional",
                    cardParagraph: "Fashion",
                    cardDifficult: "Advanced",
                    cardDuration: "6 lectures",
                    cardHours: "6 hours",
                    cardButton: true,
                    cardPrice: "$61"
                },
                {
                    cardImage: "../src/assets/img/communication.jpeg",
                    cardTitle: "Design Instruments for Communication",
                    cardParagraph: "Communication",
                    cardDifficult: "Intermediate",
                    cardDuration: "6 lectures",
                    cardHours: "6 hours",
                    cardButton: false,
                    cardPrice: "$62"
                },
                {
                    cardImage: "../src/assets/img/art.jpg",
                    cardTitle: "Make your Concept Right and Beatiful",
                    cardParagraph: "Art",
                    cardDifficult: "Intermediate",
                    cardDuration: "6 lectures",
                    cardHours: "6 hours",
                    cardButton: false,
                    cardPrice: "$63"
                },
                {
                    cardImage: "../src/assets/img/bicycling.jpeg",
                    cardTitle: "Road Bike Manual or How to Be a Champion",
                    cardParagraph: "Electronic",
                    cardDifficult: "Bicycling",
                    cardDuration: "6 lectures",
                    cardHours: "6 hours",
                    cardButton: false,
                    cardPrice: "$64"
                },
            ],
            cardsCourses: [
                {
                    icon: "fa-solid fa-briefcase",
                    title: "Entrepreneurship",
                    paragraph: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsum debitis vel quis non cupiditate voluptas veritatis voluptatem natus! Error quae veniam corporis fuga et accusamus ipsum nesciunt omnis rerum blanditiis.",
                },
                {
                    icon: "fa-solid fa-rocket",
                    title: "Accelerated learning",
                    paragraph: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsum debitis vel quis non cupiditate voluptas veritatis voluptatem natus! Error quae veniam corporis fuga et accusamus ipsum nesciunt omnis rerum blanditiis.",
                },
                {
                    icon: "fa-solid fa-thumbs-up",
                    title: "Productivity",
                    paragraph: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsum debitis vel quis non cupiditate voluptas veritatis voluptatem natus! Error quae veniam corporis fuga et accusamus ipsum nesciunt omnis rerum blanditiis.",
                },
                {
                    icon: "fa-solid fa-gear",
                    title: "Life coaching",
                    paragraph: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsum debitis vel quis non cupiditate voluptas veritatis voluptatem natus! Error quae veniam corporis fuga et accusamus ipsum nesciunt omnis rerum blanditiis.",
                },
            ],
            email: '',
            utentsRecencions: [
                {
                    image: "../src/assets/img/1-person.jpg",
                    title: "Fantastic",
                    vote: 4,
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi nobis libero quae dolorem odit rem ipsa quos veritatis explicabo possimus."
                },
                {
                    image: "../src/assets/img/2-person.jpg",
                    title: "Paints on the future",
                    vote: 5,
                    text: "The response to your MasterStudy has been really overwhelming! Those who partecipated in the workshop are spreading the word here on campus and the 'buzz' is on. The VP of Instruction wants you to come back! Her goal is to have more faculty trained. She also wants to attend a workshop herself. Our President told me MasterStudy needs to be the cornerstone of our success program."
                },
                {
                    image: "../src/assets/img/3-person.jpg",
                    title: "Very helpful",
                    vote: 3,
                    text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. At aperiam ipsam ab obcaecati et unde doloremque autem minima aliquam quisquam, architecto pariatur commodi aspernatur repellat cumque nostrum aut neque fugit doloribus. Laudantium consectetur modi quaerat exercitationem explicabo quidem amet reiciendis!"
                }
            ],
            active: 1,
        }
    },
    methods: {
        subscribe() {
            // console.log(this.email)
            alert('Complimenti! Registrazione effettutata al corso di MasterStudy');
            this.email = '';
        },
        prevAndNext(button) {
            // console.log(button)
            if(button == 'prev') {
                if(this.active > 0) {
                    this.active--
                }else {
                    this.active = this.utentsRecencions.length - 1
                }
            }else {
                if(this.active < this.utentsRecencions.length - 1) {
                    this.active++
                }else {
                    this.active = 0
                }
            }
        }
    }
}
</script>

<template>
    <main>
        <section class="first-section position-relative">
            <div class="text-bg position-absolute">
                <h2 class="fw-bold">
                    Start your human <span>Revolution</span> today
                </h2>
                <p class="size">
                    A wonderful serenity has taken possession of my entire soul, like these sweet mornings of spring which enojoy with my whole heart.
                </p>
            </div>
            <div class="offer rounded position-absolute w-100 bottom-0">
                <div class="d-flex">
                    <div class="col-6 p-4">
                        <h4 class="fw-bold p-2">
                            <span class="mini-text-h4">Limited sale:</span> All courses with 55% off
                        </h4>
                        <form @submit.prevent="subscribe()">
                            <div class="input-group mb-3 bg-white rounded-pill">
                                <input type="email" class="form-control bg-transparent border border-0 my-shadow" placeholder="Enter your email"  aria-describedby="button-addon2" v-model="email" required>
                                <button class="btn rounded-pill" type="submit" id="button-addon2">
                                    SUBSCRIPE
                                </button>
                            </div>
                        </form>
                    </div>
                    <div class="col-6 p-4">
                        <div class="d-flex">
                            <div class="col-3">
                                <p class="text-white">
                                    26
                                </p>
                                <p class="fw-bold mb-0">
                                    Days
                                </p>
                            </div>
                            <div class="col-3">
                                <p class="text-white">
                                    01
                                </p>
                                <p class="fw-bold mb-0">
                                    Hours
                                </p>
                            </div>
                            <div class="col-3">
                                <p class="text-white">
                                    47
                                </p>
                                <p class="fw-bold mb-0">
                                    Minutes
                                </p>
                            </div>
                            <div class="col-3">
                                <p class="text-white">
                                    34
                                </p>
                                <p class="fw-bold mb-0">
                                    Seconds
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section class="second-section">
            <div class="my-container">
                <div class="row">
                    <div class="col-6">
                        <h3 class="fw-bold">
                            Hey there, my name is John Doe. I'm the founder of the Brain Academy.
                        </h3>
                        <img src="../assets/img/sign.jpg" alt="Firma John Doe">
                    </div>
                    <div class="col-6">
                        <p>
                            A wonderful serenity has taken possession of my entire soul, like these sweet mornings of spring which i enjoy with my whole heart. I am alone, and feel the charm of existence in this spot, which was created for the bliss of souls like mine. I am so happy, my dear friend, so absorbed in the exquisite sense of mere tranquill existence, that i neglect my talents. When, while the lovely valley teems with vapour around me, and the meridian sun strikes the upper surface of the impenetrable follage of my trees, and but a few stray gleams steal into the inner sanctuary.
                        </p>
                    </div>
                </div>
            </div>
        </section>
        <section class="third-section">
            <div class="my-container">
                <h2 class="text-center fw-bold pt-5 mb-5">
                    New Courses
                </h2>
                <div class="row">
                    <div class="col-4 pb-5" v-for="(card, cardIndex) in cardsNewCourses" :key="cardIndex">
                        <div class="card" style="width: 18rem;">
                            <div class="container-image position-relative">
                                <img :src="card.cardImage" class="card-img-top" :alt="card.cardParagraph">
                                <button class="btn btn-primary position-absolute" v-if="card.cardButton">
                                    SPECIAL
                                </button>
                                <div class="price position-absolute h-100 w-100">
                                    {{ card.cardPrice }}
                                </div>
                            </div>
                            <div class="card-body">
                                <h5 class="card-title fw-bold">
                                    {{ card.cardTitle }}
                                </h5>
                                <p class="card-text">
                                    {{ card.cardParagraph }}
                                </p>
                                <div class="row">
                                    <div class="col-4 pe-0">
                                        <i class="fa-solid fa-signal"></i>
                                        <span>
                                            {{ card.cardDifficult}}
                                        </span>
                                    </div>
                                    <div class="col-4 pe-0">
                                        <i class="fa-solid fa-list"></i>
                                        <span>
                                            {{ card.cardDuration}}
                                        </span>
                                    </div>
                                    <div class="col-4">
                                        <i class="fa-regular fa-clock"></i>
                                        <span>
                                            {{ card.cardHours}}
                                        </span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="text-center pt-4 pb-5 container-button">
                    <button class="text-white rounded-pill">
                        LOAD MORE
                    </button>
                </div>
            </div>
        </section>
        <section class="fourth-section">
            <div class="my-container">
                <div class="row">
                    <div class="col-5">
                        <div class="text-center">
                            <h2>
                                Get My Exclusive Investing Book just fot $19.50
                            </h2>
                            <p class="text-white fst-italic">
                                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Amet architecto tenetur perspiciatis eos porro adipisci, ad eveniet reprehenderit ipsum omnis.
                            </p>
                            <a href="https://www.amazon.it/Master-your-focus-Concentration-Productivity/dp/B0C2SW3CZY/ref=sr_1_17_sspa?__mk_it_IT=ÅMÅŽÕÑ&crid=3N7BZMOBJBW2&keywords=master+study+book+template&qid=1690298997&sprefix=master+study+book+template%2Caps%2C96&sr=8-17-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9tdGY&psc=1" target="_blank">
                                <img src="../assets/img/amazon.png" alt="Amazon">
                            </a>
                        </div>
                    </div>
                    <div class="col-7">
                        <img src="../assets/img/book.png" alt="Book" class="pt-4">
                    </div>
                </div>
            </div>
        </section>
        <section class="fiveth-section">
            <div class="my-container">
                <h2 class="text-center fw-bold mt-5">
                    Why my Courses?
                </h2>
                <div class="row">
                    <div class="col-5 mt-5 border-cards" v-for="(course, courseIndex) in cardsCourses" :key="courseIndex">
                        <div class="d-flex">
                            <div class="col-3">
                                <i :class="course.icon"></i>
                            </div>
                            <div class="col-9">
                                <h4 class="fw-bold">
                                    {{ course.title}}
                                </h4>
                                <p>
                                    {{ course.paragraph }}
                                </p>
                            </div>
                        </div>
                    </div>
                    <!-- <div class="col-6">
                        card
                    </div>
                    <div class="col-6">
                        card
                    </div>
                    <div class="col-6">
                        card
                    </div> -->
                </div>
            </div>
        </section>
        <section class="sixth-section">
            <div class="my-container h-100">
                <div class="row h-100 justify-content-center align-items-center">
                    <div class="col-3 text-white d-flex justify-content-center align-items-center">
                        <div class="col-4 text-white">
                            <i class="fa-solid fa-user-group"></i>
                        </div>
                        <div class="col-8 text-white">
                            <p>
                                3195
                            </p>
                            <p>
                                Online learner
                            </p>
                        </div>
                    </div>
                    <div class="col-3 text-white d-flex justify-content-center align-items-center">
                        <div class="col-4 text-white">
                            <i class="fa-solid fa-film"></i>
                        </div>
                        <div class="col-8 text-white">
                            <p>
                                23
                            </p>
                            <p>
                                Video courses
                            </p>
                        </div>
                    </div>
                    <div class="col-3 text-white d-flex justify-content-center align-items-center">
                        <div class="col-4 text-white">
                            <i class="fa-regular fa-image"></i>
                        </div>
                        <div class="col-8 text-white">
                            <p>
                                437
                            </p>
                            <p>
                                Sliders & Images
                            </p>
                        </div>
                    </div>
                    <div class="col-3 text-white d-flex justify-content-center align-items-center">
                        <div class="col-4 text-white">
                            <i class="fa-solid fa-thumbs-up"></i>
                        </div>
                        <div class="col-8 text-white">
                            <p>
                                1440
                            </p>
                            <p>
                                Excellent Reviews
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section class="seventh-section">
            <div class="my-container">
                <div class="text-center">
                    <h2 class="fw-bold">
                        What Students Says?
                    </h2>
                    <div class="container-image position-relative">
                        <button class="position-absolute prev" @click="prevAndNext('prev')">
                            <i class="fa-solid fa-arrow-left-long"></i>
                        </button>
                        <button class="position-absolute next" @click="prevAndNext('next')">
                            <i class="fa-solid fa-arrow-right-long"></i>
                        </button>
                        <img :src="utent.image" :alt="utent.title" class="rounded-circle" :class="utentIndex == active ? 'active' : ''" v-for="(utent, utentIndex) in utentsRecencions" :key="utentIndex">
                        <template v-for="(utent, utentIndex) in utentsRecencions" :key="utentIndex">
                            <div class="container-star" v-if="utentIndex == active">
                                <h6 class="fw-bold">
                                    {{ utent.title }}
                                </h6>
                                <i class="fa-solid fa-star" v-for="(star, index) in utent.vote" :key="index"></i>
                                <p class="text-center">
                                    "{{ utent.text }}"
                                </p>
                            </div>
                        </template>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
main {
    .first-section {
        background-image: url(../assets/img/slide-1.jpg);
        background-size: contain;
        background-repeat: no-repeat;
        height: 700px;
        width: 100%;

        span {
            color: $divAndFooterBg;
        }
        .offer {
            background-color: $divAndFooterBg;
            max-width: 1052px;
            left: 15%;
        }
        .my-shadow {
            box-shadow: none;
        }
        button {
            background-color: $button;
            color: white;
        }
        button:hover {
            filter: invert(1);
        }
        .mini-text-h4 {
            color: white;
        }
        .text-bg {
            width: 400px;
            top: 25%;
            left: 45%;
            
            .size {
                font-size: small;
            }
        }
        .text-white {
            font-size: 50px;
            margin-bottom: 0;
        }
    }
    .second-section {
        margin: 100px 0;
        .my-container {
            max-width: 992px;
            margin: 0 auto;
        }
        .col-6 > img {
            padding: 20px 0 0 150px;
        }
        .col-6 > p {
            font-size: small;
            line-height: 25px;
        }
    }
    .third-section {
        background-color: $sectionMainBg;
        .my-container {
            max-width: 992px;
            margin: 0 auto;
        }
        .container-button > button {
            margin: 30px 0 20px 0;
            background-color: #F2B91E;
            padding: 10px;
            border: none;
            font-size: small;
        }
        .col-4 h5, .col-4 p{
            text-align: center;
        }
        .col-4 p {
            color: $colorTextCard;
            font-size: small;
            padding-bottom: 30px;
            border-bottom: 1px solid $colorTextCard;
        }
        .container-image > button {
            top: 0;
            right: 0;
            margin: 10px;
            font-size: xx-small;
            padding: 5px;
            background-color: #F2B91E;
            border: none;
            z-index: 999;
        }
        .col-4 span {
            font-size: x-small;
            vertical-align: middle;
            padding-left: 2px;
        }
        .col-4 i {
            color: $divAndFooterBg;
        }
        .price {
            top: 0;
            left: 0;
            color: white;
            font-size: x-large;
            background-color: rgba($color: #000000, $alpha: 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            visibility: hidden;
            opacity: 0;
        }
        .card:hover .price{
            visibility: visible;
            opacity: 1;
        }
        button:hover {
            background-color: #D9A61B;
        }
        .card {
            cursor: pointer;
        }
    }
    .fourth-section {
        background-image: url(../assets/img/bg-slider.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
        .my-container {
            max-width: 992px;
            margin: 0 auto;
        }
        .col-5 h2 {
            color: $divAndFooterBg;
            font-weight: bold;
        }
        .col-5 > div {
            padding-top: 100px;
        }
        a:hover {
            filter: contrast(0.5);
        }
    }
    .fiveth-section {
        .my-container {
            max-width: 992px;
            margin: 0 auto;
        }
        .col-5 {
            box-shadow: 2px 2px 10px 10px $colorTextCard;
            padding: 30px 15px;
            margin-right: 80px;
        }
        .col-5:hover {
            background-color: $divAndFooterBg;
        }
        .col-5:hover i {
            color: white;
        }
        .border-cards {
            border-left: 5px solid $divAndFooterBg;
        }
        .col-3 > i {
            font-size: 70px;
            color: $divAndFooterBg;
        }
        .col-9 > p {
            font-size: small;
            color: $colorTextCard;
        }
    }
    .sixth-section {
        height: 400px;
        background-image: url(../assets/img/bg-sixth-section.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        margin-top: 80px;
        .my-container {
            max-width: 992px;
            margin: 0 auto;
        }
        * i {
            font-size: 50px;
        }
        .col-8 > :first-child {
            color: $divAndFooterBg;
            font-size: xx-large;
            margin-bottom: 0;
            font-weight: bold;
        }
    }
    .seventh-section {
        .my-container {
            max-width: 992px;
            margin: 0 auto;

            .text-center > h2 {
                margin: 40px 0;
            }
            button {
                width: 50px;
                background-color: transparent;
                border: none;
                i {
                    font-size: x-large;
                }
            }
            .prev {
                left: 20%;
                top: 10%;
            }
            .next {
                right: 20%;
                top: 10%;
            }
            .container-image {
                min-height: 400px;
                img {
                    width: 60px;
                    margin-bottom: 20px;
                    margin: 0 10px 15px;
                } 
                .active {
                    width: 100px;
                }
            }
            .container-star { 
                width: 300px;
                margin: 0 auto;
                
                i {
                    color: $divAndFooterBg;
                }
                p {
                    margin: 30px 0;
                    font-size: small;
                }
            }
        }
    }
}


</style>
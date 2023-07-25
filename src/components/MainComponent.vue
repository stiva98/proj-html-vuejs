<script>
export default {
    name: "MainComponent",
    data() {
        return {

        }
    },
    methods: {

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
                        <div class="input-group mb-3 bg-white rounded-pill">
                            <input type="text" class="form-control bg-transparent border border-0" placeholder="Enter your email"  aria-describedby="button-addon2">
                            <button class="btn rounded-pill" type="button" id="button-addon2">SUBSCRIPE</button>
                        </div>
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
        button {
            background-color: $button;
            color: white;
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
        margin-top: 100px;
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
}


</style>
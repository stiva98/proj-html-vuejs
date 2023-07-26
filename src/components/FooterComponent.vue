<script>
export default {
    name: "FooterComponent",
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>

<template>
    <footer>
        <div class="my-container">
            <div class="row">
                <div class="col-3">
                    <h5>
                        ABOUT
                    </h5>
                    <p>
                        Masterstudy is Education WordPress theme featured by Learning Management System (LMS) for online education. Developed by StylemixThemes
                    </p>
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </div>
                <div class="col-3">
                    <h5>
                        CONTACT
                    </h5>
                    <p>
                        USA, California 20, First Avenue, California
                    </p>
                    <p>
                        Tel.: +1 212 458 300 32 <br>
                        Fax: +1 212 375 24 14
                    </p>
                    <p>
                        info@masterstudy.com
                    </p>                   
                </div>
                <div class="col-3">
                    <h5>
                        PAGES
                    </h5>
                    <div class="d-flex">
                        <div class="col-6">
                            <ul>
                                <li>
                                    <a href="">
                                        Blog
                                    </a>
                                </li>
                                <li>
                                    <a href="">
                                        Home
                                    </a>
                                </li>
                                <li>
                                    <a href="">
                                        Shortcodes
                                    </a>
                                </li>
                            </ul>
                        </div>
                        <div class="col-6">
                            <ul>
                                <li>
                                    <a href="">
                                        Courses
                                    </a>
                                </li>
                                <li>
                                    <a href="">
                                        Membership A...
                                    </a>
                                </li>
                                <li>
                                    <a href="">
                                        Typography
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col-3">
                    <h5>
                        BLOG
                    </h5>
                    <div class="d-flex">
                        <div class="col-4">
                            <img src="../assets/img/photo-1-footer.jpeg" alt="foto-1">
                        </div>
                        <div class="col-8">
                            <h6 class="fw-bold">
                                Our main target is to "Developing Yourself as a Leader"
                            </h6>
                            <p class="text-last-column">
                                - August 9, 2018
                            </p>
                        </div>
                    </div>
                    <div class="d-flex">
                        <div class="col-4">
                            <img src="../assets/img/photo-2-footer.jpeg" alt="foto-2">
                        </div>
                        <div class="col-8">
                            <h6 class="fw-bold">
                                Those Other Collage Expense You Aren't Thinking About
                            </h6>
                            <p class="text-last-column">
                                - June 3, 2015
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
footer {
    background-color: $divAndFooterBg;
    .my-container {
        max-width: 992px;
        margin: 0 auto;
        padding: 50px 0;
    }
    * h5 {
        font-weight: bold;
        margin-bottom: 16px;
    }
    * p {
        color: $colorTextFooter;
        font-size: small;
    }
    * i {
        padding-right: 10px;
        color: $colorTextFooter #333333;
        cursor: pointer;
    }
    * i:hover {
        color: white;
    }
    p:last-child:hover {
        color: white;
        cursor: pointer;
    }
    ul {
        padding-left: 15px;

        li{
            margin-bottom: 15px;
            font-size: small;
        }
        a{
            color: $colorTextFooter;
            text-decoration: none;
        }
        li:hover{
            color: white;
        }
        li:hover a{
            color: white;
        }
    }
    .d-flex {
        margin-bottom: 15px;
        .col-8 {
            margin-left: 15px;
        }
        img {
            width: 100%;
        }
        h6 {
            font-size: small;
        }
        .text-last-column {
            color: $colorTextCard;
        }
        .text-last-column:hover {
            color: $colorTextCard;
            cursor: default;
        }
    }

}
</style>
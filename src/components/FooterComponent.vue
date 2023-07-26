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
                </div>
                <div class="col-3">
                    <h5>
                        BLOG
                    </h5>
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
}
</style>
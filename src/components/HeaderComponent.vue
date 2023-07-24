<script>
export default {
    name: "HeaderComponent",
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="row align-items-center">
                <div class="col-3">
                    <img src="../assets/img/MasterStudy-1.svg" alt="">
                </div>
                <div class="col-6">
                    <ul class="d-flex justify-content-end list-unstyled mb-0">
                        <li>
                            <a href="#">Courses</a>
                        </li>
                        <li>
                            <a href="#">Course Formats   
                            </a>
                        </li>
                        <li>
                            <a href="#" class="position-relative">Add Course</a>
                                <span class="translate-middle badge bg-danger">
                                    NEW
                                </span> 
                        </li>
                        <li>
                            <a href="#">Pages</a>
                        </li>
                        <li>
                            <a href="#">Demos</a>
                        </li>
                    </ul>
                </div>
                <div class="col-3">
                    <i class="fa-brands fa-linkedin"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-twitter"></i>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
header {
    .row {
        padding: 30px 0;
    }
    li {
        padding: 0 10px;
        cursor: pointer;
        position: relative;

        a {
            text-decoration: none;
            color: black;
        }
        a:hover {
            color: $divAndFooterBg;
        }
        &::after {
            content: '';
            height: 3px;
            width: 100%;
            display: block;
            background-color: $divAndFooterBg;
            position: absolute;
            bottom: 0;
            left: 0;
            visibility: hidden;
            opacity: 0;
        }
        &:hover::after {
            visibility: visible;
            opacity: 1;
        }
        span {
            position: absolute;
            top: -20%;
            left: 88%;
        }
    }
    i {
        padding: 0 5px;
        cursor: pointer;
    }
    i:hover {
            color: $divAndFooterBg;
    }
}
</style>
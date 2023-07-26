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
        <div class="my-container">
            <div class="row align-items-center">
                <div class="col-3">
                    <img src="../assets/img/MasterStudy-1.svg" alt="">
                </div>
                <div class="col-7 p-0">
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
                <div class="col-2 p-0 text-end">
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
    .my-container {
        max-width: 992px;
        margin: 0 auto;
    }
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
        &:hover a {
            color: $divAndFooterBg;
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
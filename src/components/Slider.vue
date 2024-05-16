<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation } from 'swiper/modules'
import "swiper/css"
import 'swiper/css/navigation'

const slides = [{
    icon: "/src/assets/Exprerian/CompuloanLogo.png",
    image: "/src/assets/Exprerian/Carousal1.png",
    description: "The PurQ service provides academic enrolment or qualification verification on an individual, in respect of an extensive list of participating academic institutions."
},
{
    icon: "/src/assets/Exprerian/ColumbusLogo.png",
    image: "/src/assets/Exprerian/Carousal1 – 1.png",
    description: "Columbus provides highly effective search functionalities that enable you to efficiently search for missing debtors, obtain their contact information, and establish their whereabouts..."
},
{
    icon: "/src/assets/Exprerian/CodixLogo.png",
    image: "/src/assets/Exprerian/Carousal1 – 2.png",
    description: "This service allows a 3rd party to retrieve a PDF Consumer Credit Report based on a previous enquiry or by doing a full enquiry"
},
{
    icon: "/src/assets/Exprerian/XceleratorLogo.png",
    image: "/src/assets/Exprerian/Carousal1 – 3.png",
    description: "The Employment Confidence Index (ECI) is a tool used to indicate the most probable employer listed on Experian’s credit bureau."
},
{
    icon: "/src/assets/Exprerian/AASLogo.png",
    image: "/src/assets/Exprerian/Carousal1 – 4.png",
    description: "The Identity Verification Service provides real-time verification on the identity of a consumer.."
},
{
    icon: "/src/assets/Exprerian/IncomePredictorLogo.png",
    image: "/src/assets/Exprerian/Carousal1 – 5.png",
    description: "Experian's Know Your Customer service, provides subscribers with consumer identity verification, contact numbers, address and employment information."
}
]
const slideBreaks = {
    320: {
        slidesPerView: 1,
        spaceBetween: 10
    },
    1024: {
        slidesPerView: 2,
        spaceBetween: 30
    },
    1366: {
        slidesPerView: 3,
        spaceBetween: 30
    }
}

const openMenu = () => {
    const menu = document.querySelector(".side-nav");
    menu.classList.add("open");
}

const closeMenu = () => {
    const menu = document.querySelector(".side-nav.open");
    menu.classList.remove("open");
}
</script>
<template>
    <section class="carousel">
        <div class="container-fluid">
            <div class="row">
                <div class="col-12 text-center">
                    <h2 class="power-title">Powerful Data <span> <img src="/src/assets/Exprerian/DrivenWording.png"
                                alt=""></span> Tools to Help <br /> Your Thrive</h2>
                    <p class="power-sub-titile">Our data-driven products can significantly reduce costs while increasing
                        your overall profit margins</p>
                </div>
            </div>
            <div class="row justify-content-center align-items-center">
                <div class="col-1 slider-arrow">
                    <i class="bi bi-chevron-compact-left button-prev"></i>
                </div>
                <div class="col-10">
                    <Swiper :class="'swiper-slide-container'" :slides-per-view="3" :modules="[Navigation]"
                        :navigation="{ nextEl: '.button-next', prevEl: '.button-prev' }" :loop="true"
                        :breakpoints="slideBreaks">
                        <SwiperSlide class="swiper-slide" v-for="slide in slides" :key="slide">
                            <span class="align-self-center"><img :src="slide.icon"></span>
                            <img class="align-self-center" :src="slide.image">
                            <p class="slide-description">{{ slide.description }}</p>
                            <hr class="solid">
                            <button class="slider-button" @click="openMenu()">Enquire</button>
                        </SwiperSlide>
                    </Swiper>
                </div>
                <div class="col-1 slider-arrow">
                    <i class="bi bi-chevron-compact-right button-next"></i>
                </div>
            </div>
        </div>
    </section>
    <section class="side-nav">
        <i class="bi bi-x-lg d-flex justify-content-end close-icon  " @click="closeMenu()"></i>
        <div class="container">
            <div class="row pt-3">
                <div class="col-6 ">
                    <h4>Enquiry Form</h4>
                </div>
                <div class="col-6">
                    <i class="bi bi-cloud rounded-circle cloud-icon d-flex justify-content-end"></i>
                </div>
            </div>
            <div class="row">
                <div class="menu">
                    <form>
                        <div class="form-group mt-3">
                            <label for="exampleInputEmail1">Name</label>
                            <input type="email" class="form-control">
                        </div>
                        <div class="form-group mt-3">
                            <label for="exampleInputEmail1">Email Address</label>
                            <input type="email" class="form-control">
                        </div>
                        <div class="form-group mt-3">
                            <label for="exampleInputPassword1">Phone Number</label>
                            <input type="text" class="form-control">
                        </div>
                        <select class="form-select mt-3">
                            <option selected>Columbus</option>
                            <option value="1">Compoloan</option>
                            <option value="2">Codix</option>
                            <option value="3">Xcelerator</option>
                            <option value="4">Affordability Assessment Service</option>
                            <option value="5">Income Predictor</option>
                        </select>
                        <div class="form-group mt-3">
                            <label for="exampleFormControlTextarea1">Your Question</label>
                            <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
                        </div>
                        <div class="form-group d-flex justify-content-end">
                            <button type="submit"
                                class="form-group btn btn-theme-form mt-4 "><i class="bi bi-send-fill ml-2 "></i>Send</button>
                        </div>
                    </form>
                    <div class="row mt-5">
                        <div class="col-12">
                            <h5>Frequent Asked Questions</h5>
                            <div class="row mt-3">
                                <div class="accordion" id="accordionExample">
                                    <div class="accordion-item">
                                        <h2 class="accordion-header" id="headingOne">
                                            <button class="accordion-button" type="button" data-bs-toggle="collapse"
                                                data-bs-target="#collapseOne" aria-expanded="true"
                                                aria-controls="collapseOne">
                                                <strong>How long does it take to activate my account after my
                                                    purchase?.</strong>
                                            </button>
                                        </h2>
                                        <div id="collapseOne" class="accordion-collapse collapse show"
                                            aria-labelledby="headingOne" data-bs-parent="#accordionExample">
                                            <div class="accordion-body">
                                                How long does it take to activate my account after my purchase?.
                                            </div>
                                        </div>
                                    </div>
                                    <div class="accordion-item">
                                        <h2 class="accordion-header" id="headingTwo">
                                            <button class="accordion-button collapsed" type="button"
                                                data-bs-toggle="collapse" data-bs-target="#collapseTwo"
                                                aria-expanded="false" aria-controls="collapseTwo">
                                                <strong>How do I cancel my membership for a specific product?</strong>
                                            </button>
                                        </h2>
                                        <div id="collapseTwo" class="accordion-collapse collapse"
                                            aria-labelledby="headingTwo" data-bs-parent="#accordionExample">
                                            <div class="accordion-body">
                                                How do I cancel my membership for a specific product?
                                            </div>
                                        </div>
                                    </div>
                                    <div class="accordion-item">
                                        <h2 class="accordion-header" id="headingThree">
                                            <button class="accordion-button collapsed" type="button"
                                                data-bs-toggle="collapse" data-bs-target="#collapseThree"
                                                aria-expanded="false" aria-controls="collapseThree">
                                                <strong>Do you have fraud prevention tools</strong>
                                            </button>
                                        </h2>
                                        <div id="collapseThree" class="accordion-collapse collapse"
                                            aria-labelledby="headingThree" data-bs-parent="#accordionExample">
                                            <div class="accordion-body">
                                                Do you have fraud prevention tools
                                            </div>
                                        </div>
                                    </div>
                                    <div class="accordion-item">
                                        <h2 class="accordion-header" id="headingThree">
                                            <button class="accordion-button collapsed" type="button"
                                                data-bs-toggle="collapse" data-bs-target="#collapseThree"
                                                aria-expanded="false" aria-controls="collapseThree">
                                                <strong>Do you have a call centre I can contact</strong>
                                            </button>
                                        </h2>
                                        <div id="collapseThree" class="accordion-collapse collapse"
                                            aria-labelledby="headingThree" data-bs-parent="#accordionExample">
                                            <div class="accordion-body">
                                                Do you have a call centre I can contact
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style>
.carousel {
    background-image: url("/src/assets/Exprerian/BG3.png");
    background-size: cover;
    background-position: center center;
    background-repeat: no-repeat;
    min-height: 1000px;
}

.carousel .container-fluid {
    padding: 100px 180px;
}

.power-title,
.power-sub-titile {
    color: #ffffff;
}

.power-title {
    font-size: 70px;
}

.power-sub-titile {
    font-size: 25px;
    margin-bottom: 70px;
}

.swiper-slide {
    display: flex;
    flex-direction: column;
    padding: 1rem;
    border-radius: 5px;
    background-color: #ffffff;
    height: 100%;
}

.swiper-slide img {
    object-fit: cover;
    width: 100%;
}

.slide-description {
    word-wrap: break-word;
    flex-grow: 1
}

.slider-arrow {
    font-size: 50px;
    text-align: center;
    color: #ffffff;
}

.slider-button {
    align-self: end;
    margin-bottom: 10px;
    margin-right: 10px;
    background: #ffffff;
    border: 1px solid #E63888;
    color: #E63888;
    border-radius: 8px;
    height: 32px;
    width: 70px;
}

.side-nav {
    position: fixed;
    top: 0;
    right: -350px;
    width: 350px;
    height: 100vh;
    background-color: #ffffff;
    color: #000;
    z-index: 99;
    overflow-y: auto;
}

.open {
    right: 0;
}

.close-icon {
    color: #004691;
    padding: 12px;
    -webkit-text-stroke: 1px
}

.cloud-icon {
    font-size: 2rem;
}

.chevron-compact-down-icon {
    -webkit-text-stroke: 1px
}
</style>
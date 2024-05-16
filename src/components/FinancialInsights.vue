<script setup></script>

<template>
    <section class="financial">
        <div class="container-fluid align-content-end">
            <div class="row">
                <div class="col-6 col-sm-12 col-lg-6 col-xl-6 col-super-4 align-self-end">
                    <img class="image" src="/src/assets/Exprerian/Infographic2.png">
                </div>
                <div class="col-6 col-sm-12 col-lg-6 col-xl-6 col-super-8 align-content-center">
                    <h2 class="financial-title mb-5"><span>Financial <img src="/src/assets/Exprerian/InsightsWording.png"> in the <br>Palm of Your Hands </span></h2>
                    <p class="financial-text">Drive intelligent decisions, new product innovation and better targeting through insight <br>
                    and technology. Helping to deliver a frictionless digital customer experience.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
    .financial {
        background-image: url("/src/assets/Exprerian/BG2.png");
        background-size: cover;
        background-position: center center;
        background-repeat: no-repeat;
    }
    .financial .container-fluid {
        padding-left: 109px;
        padding-right: 109px;
        min-height: 600px;
    }
    .image {
        height: 480px;
    }
    .financial .financial-title,
    .financial .financial-text {
        color: #ffffff;
    }
    .financial .financial-title {
        font-size: 70px;
    }
    .financial .financial-text {
        font-size: 18px;
    }
    @media screen and (max-width: 1600px) {
        .financial .container-fluid {
            padding-left: 15px;
        }
    }
    @media screen and (min-width: 1601px) {
        .financial .container-fluid {
            padding-left: 218px;
        }
    }

    @media screen and (max-width: 699px) {
        .financial .container-fluid  {
            padding: 15px;
        }
        
        .financial .financial-title {
            font-size: 50px;
            text-align: center;
        }
    }
</style>
<script setup>
    import Infomation from '../../src/Information.json'

    const dataTable = Infomation;
 </script>

<template>
    <section class="py-5">
        <div class="container">
            <div class="row">
                <div class="col-12 text-center">
                    <h2 class="info-title">Innovated Products That Gives You all <br> The <span><img src="/src/assets/Exprerian/InformationWording – 1.png" alt=""></span> You Need</h2>
                </div>
            </div>
            <div class="row">
                <div class="col-12">
                    <div class="info-table">
                        <div class="row">
                            <div class="col-md-2 headings">Product</div>
                            <div class="col-md-2 headings">Feature #1</div>
                            <div class="col-md-2 headings">Feature #2</div>
                            <div class="col-md-2 headings">Feature #3</div>
                            <div class="col-md-2 headings">Feature #4</div>
                            <div class="col-md-2 headings">Feature #5</div>
                        </div>
                        <div class="row" v-for="data in dataTable" :key="data">
                            <div class="col-md-2 fields"> {{data.product}}</div>
                            <div class="col-md-2 fields text-center"><i v-if="data.feature1 === 'x'" class="bi bi-check-circle-fill check-icon"></i></div>
                            <div class="col-md-2 fields text-center"><i v-if="data.feature2 === 'x'" class="bi bi-check-circle-fill check-icon"></i></div>
                            <div class="col-md-2 fields text-center"><i v-if="data.feature3 === 'x'" class="bi bi-check-circle-fill check-icon"></i></div>
                            <div class="col-md-2 fields text-center"><i v-if="data.feature4 === 'x'" class="bi bi-check-circle-fill check-icon"></i></div>
                            <div class="col-md-2 fields text-center"><i v-if="data.feature5 === 'x'" class="bi bi-check-circle-fill check-icon"></i></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
    .info-title {
        font-size: 50px;
        font-weight: bold;
        color: #1D4F91;
    }
    .headings {
         padding-top: 10px;
         padding-bottom: 10px;
         border: 1px solid #6D2077;
         background-color: #F0E9F1;
     }
     .fields {
         padding-top: 10px;
         padding-bottom: 10px;
         border: 1px solid #6D2077;
         justify-content: center;
         background-color: #F0E9F1;
         color: #333333;
    
     }
    .fields:first-child {
        font-weight: bold;
    }
    .check-icon {
        color: green;
        background-color:#F0E9F1;
    }
</style>
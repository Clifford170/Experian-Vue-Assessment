<script setup></script>

<template>
    <footer class="footer">
        <div class="container-fuid">
            <div class="row">
                <div class="col-sm-12 col-md-4">
                    <img class="footer-logo"src="/src/assets/Exprerian/ExperianLogo.png" alt="Experian Logo">
                </div>
                <div class="col-sm-12 col-md-8">
                    <ul class="footer-nav justify-content-end">
                        <li class="footer-nav-items"><a href="#">TERMS AND CONDITIONS</a></li>
                        <li class="footer-nav-items"><a href="#">PRIVACY POLICY</a></li>
                        <li class="footer-nav-items"><a href="#">PRESS</a></li>
                        <li class="footer-nav-items"><a href="#">CAREER</a></li>
                        <li class="footer-nav-items"><a href="#">INVESTOR RELATIONS</a></li>
                    </ul>
                </div>
            </div>
    
            <div class="row mt-3 copyright">
                <div class="col-12">
                    <p>© 2022 Experian South Africa (Pty) Ltd. All Rights Reserved.</p>
                    <p>Experian is a registered credit bureau in terms of the National Credit Act (NCA) Registration No: 2006/010440/07 l NCR No: NCRCB16</p>
                </div>
            </div>
        </div>
    </footer>
</template>

<style>
    .footer {
        padding-top: 20px;
        padding-bottom: 20px;
    }
    .footer-nav {
        display: flex;
    }
    .footer-nav-items {
        font-size: 15px;
        display: inline-flex;
        padding-left: 15px;
    }
    .footer-nav-items a {
        text-transform: uppercase;
        font-weight: bold;
        text-decoration: none;
        color: #333333;
    }
    .copyright p {
        font-size: 12px;
        color: #686868;
    }
</style>
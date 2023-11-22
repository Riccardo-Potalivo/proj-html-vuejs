<template>
    <section>
        <div class="container">
            <div class="row align-items-center ">
                <div class="col-4 d-flex flex-column align-items-center gap-3">
                    <img class="w-75" src="../assets/image/avadabarbers_footer_shop_image.png" alt="shop">
                    <a href="#" class="btn_primary">shop our range now</a>
                </div>
                
                <div class="col-4 ">
                    <img src="../assets/image/avadabarbers-logo-x2-300x104.png" width="200px" alt="logo">
                    <ul>
                        <li>Avada Barbers</li>
                        <li>123 New York Street</li>
                        <li>New York City</li>
                        <li>info@yourwebsite.com</li>
                        <li>+1 (555) 555-1212</li>
                    </ul>
                    <p>FOLLOW US</p>
                    <div class="d-flex justify-content-center gap-3">
                        <i class="fa-brands fa-facebook-f"></i>
                        <i class="fa-brands fa-x-twitter"></i>
                        <i class="fa-brands fa-instagram"></i>
                        <i class="fa-brands fa-youtube"></i>
                    </div>
                    
                </div>

                <div class="col-4 d-flex flex-column align-items-center gap-3">
                    <img class="w-75" src="../assets/image/avadabarbers_footer_appointment_image.png" alt="shop">
                    <a href="#" class="btn_primary">shop</a>
                </div>
                
            </div>
                  
        </div>
    </section>
    
    <section>
        <div class="container text-center">
            <span>© Copyright 2012 - 2023 | Avada Theme b </span>
            <a href="#">ThemeFusion </a>
            <span>| All Rights Reserved | Powered by </span>
            <a href="#">WordPress</a>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'FooterComponent'
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

* {
    color: $DarkerGrey;
}

p,
a {
    color: $PrimaryColor;
    text-decoration: none;
}

section:first-child {
    background-color: $BgFooterDarker;

    ul {
        margin: 3rem 0;
    }
    

    .col-4 {
        text-align: center;
    }

    .btn_primary {
        font-size: 0.8rem;
    }
    
}

section:last-child {
    background-color: $BgFooterDark;
    
}
.container {
    padding: 3rem 0;
}


</style>
<template>
    <section id="award_winning">
        <div class="container">
            <p class="header_description">award</p>
            <h2>Barbers</h2>
            <div class="btn_primary">meet</div>
        </div>
        <svg
            class="fusion-big-triangle-candy d-none d-lg-block " 
            xmlns="http://www.w3.org/2000/svg" 
            version="1.1" 
            width="100%" 
            height="100" 
            viewBox="0 0 100 100" 
            preserveAspectRatio="none"
        >
            <path d="M0 100 L50 2 L100 100 Z"></path>
        </svg>
    </section>

    <section id="services">
        <div class="container">
            <p class="header_description">award</p>
            <h2>Barbers</h2>
            <div class="btn_primary">meet</div>
        </div>
        <svg
            class="fusion-big-triangle-candy d-none d-lg-block " 
            xmlns="http://www.w3.org/2000/svg" 
            version="1.1" 
            width="100%" 
            height="100" 
            viewBox="0 0 100 100" 
            preserveAspectRatio="none"
        >
            <path d="M0 100 L50 2 L100 100 Z"></path>
        </svg>
    </section>
    
    <section id="products">
        <div class="container">
            <p class="header_description">award</p>
            <h2>Barbers</h2>
            <div class="btn_primary">meet</div>
        </div>
    </section>
    
    <section id="featured_products">
        <div class="container">
            <div>
                <div class="product_box">
                    <div class="box_image">
                        <img src="../assets/image/shaving_butter-600x600.png" alt="shaving butter">
                    </div>
                </div>
                <div class="product_box">
                    <p class="header_description">award</p>
                    <h2>Barbers</h2>
                    <div class="btn_primary">meet</div>
                </div>
            </div>
        </div>
    </section>
    
        <section id="blog_post">
            <svg
                class="fusion-big-triangle-candy d-none d-lg-block " 
                xmlns="http://www.w3.org/2000/svg" 
                version="1.1" 
                width="100%" 
                height="100" 
                viewBox="0 0 100 100" 
                preserveAspectRatio="none"
            >
                <path d="M0 100 L50 2 L100 100 Z"></path>
            </svg>
            <div class="container">
                <p class="header_description">award</p>
                <h2>Barbers</h2>
                <div class="btn_primary">meet</div>
            </div>
        </section>

    </template>

<script>
    export default {
        name: 'MainComponent'
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

// section background
#award_winning {
    .container {
        padding: 8em 0;
    }
    
    background-image: url(../assets/image/avadabarbers-about-introbackground.jpg);
    background-size: cover;

    svg {
        fill: $White;
    }
}

#services {
    .container {
        padding: 8em 0;
    }
    
    background-color: $White;
    background-size: cover;

    svg {
        fill: #121315;
    }
}

#products {
    .container {
        padding: 4em 0 8rem;
    }

    background-image: url(../assets/image/avadabarbers-reviewsbackground.jpg);
    background-size: cover;

    svg {
        fill: $White;
    }
}

#featured_products {
    
    position: relative;
    top: -7rem;

    .container {
        padding: 4em 0;
        > div {
            display: flex;
            border-top: solid 4px $PrimaryColor;
        }
    }
    
    .product_box:first-child {
        background-image: url(../assets/image/avadabarbers-cta-background.jpg);
        background-size: cover;
        width: 40%;
        // height: 10%;
        .box_image {
            width: 100%;
            height: 100%;
            
        }

        img {
            width: 100%;
            height: 100%;
            object-fit: scale-down;
        }
    }
    
    .product_box:last-child {
        background-color: $Black;
        width: 60%;
        text-align: left;
        padding: 4rem;
    }

}

#blog_post {
    .container {
        padding: 8em 0;
    }
    
    background-color: $LightGrey;
    background-size: cover;

    svg {
        fill: $White;
        transform: rotate(180deg);
    }
}

section {
    text-align: center;
}
.header_description {
    // font-size: 4rem;
    color: $PrimaryColor;
    text-transform: uppercase;

margin: 0;}

h2 {
    font-family: abrilfatface;
    font-size: 4rem;
    color: $DarkGrey;
}

</style>
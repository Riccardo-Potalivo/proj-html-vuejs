<template>

    <section id="award_winning">
        <div class="container">
            <p class="header_description">award winning</p>
            <h2>Pro Barbers</h2>
            <a class="btn_primary" href="#">meet your new barber</a>
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
            <p class="header_description">mens grooming</p>
            <h2>Services</h2>
            <div class="row pt-5">
                <ServiceCard
                    v-for="el in store.services"
                    :key="el"
                    :img="el.img"
                    :title="el.title"
                    :text="el.text"
                />
            </div>
            <a class="btn_primary" href="#">read about our services</a>
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
            <p class="header_description">we have you covered</p>
            <h2>Avada Grooming Products</h2>
            <a class="btn_primary" href="#">shop our product range</a>
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
                    <p class="header_description">this months featured product</p>
                    <h2>Shaving Butter</h2>
                    <p class="main_description pt-4">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque laoreet enim est, vel molestie dolor ultrices ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                    </p>
                    <a class="btn_primary" href="#">buy now</a>
                </div>
            </div>
        </div>
    </section>
        
    <section id="reviews">
        <div class="container">
            <p class="header_description">what people say</p>
            <h2>Reviews</h2>
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
            <p class="header_description">tales from the barber shop</p>
            <h2>Recent Blog Posts</h2>
            <a class="btn_primary" href="#">read more from blog</a>
        </div>
    </section>

</template>

<script>
    import { store } from '../data/store'
    import ServiceCard from './elements/ServiceCard.vue'

    export default {
        name: 'MainComponent',

        components: {
            ServiceCard
        },

        data() {
            return {
                store
            }
        }
    }
</script>

<style lang="scss">
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

    @media (max-width: 1025px) {
        display: none;
    }
    
    position: relative;
    top: -7rem;
    
    .container {
        padding: 4em 0 0;
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

#reviews {
    .container {
        padding: 4em 0;
    }

    svg {
        fill: $White;
    }
}

#blog_post {
    .container {
        padding: 6em 0;
    }
    
    background-color: $LightGrey;

    svg {
        fill: $White;
        transform: rotate(180deg);
    }
}

section {
    text-align: center;
}

.header_description {
    color: $PrimaryColor;
    text-transform: uppercase;
    margin: 0;
}

.main_description {
    line-height: 2;
    font-size: 1.2rem;
    color: $DarkerGrey;
}

h2 {
    font-family: abrilfatface;
    font-size: 4rem;
    color: $DarkGrey;
}

</style>
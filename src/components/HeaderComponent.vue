<template>
    <section>
        <div 
            id="menu"
            :class="{ 'w-100' : menuOffcanvas}"
            >
            <i 
                class="fa-solid fa-xmark fa-xl"
                :class="{ 'd-none' : !menuOffcanvas}"
                @click="menuOffcanvas = false"
            ></i>
        </div>
        <nav class="fixed-top" :class="{ 'navbar_active' : scrollCount }">
            <div class="container d-flex justify-content-between ">
                <a href="#">
                    <img src="../assets/image/avadabarbers-logo-x2-300x104.png" width="200px" alt="logo">
                </a>

                <ul>
                    <!-- <li class="text-white " id="scroll">
                        {{ scrollCount }}
                    </li> -->
                    <li id="cart_item">
                        <i class="fa-solid fa-cart-shopping"></i>
                    </li>
                    <li id="menu_item">
                        <i 
                            class="fa-solid fa-bars"
                            @click="menuOffcanvas = true"
                        ></i>     
                    </li>
                </ul>

            </div>
        </nav>
        <div 
            class="container d-flex flex-column justify-content-center align-items-md-baseline align-items-center" 
            id="main_header"
        >
            <h1>Barber Shop</h1>
            <div class="divider"></div>
            <p>The Pinnacle of Male Grooming</p>
            <a class="btn_primary" href="#">learn more</a>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        
        data() {
            
            return {
                scrollCount: 0,
                menuOffcanvas: false
            }
        },

        methods: {
            
        },

        mounted() {
            window.addEventListener("scroll", () => {
                console.log(window.scrollY)
                this.scrollCount = window.scrollY;
            });
            
        },

    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

// menu panel
#menu {
    position: fixed;
    top: 0;
    right: 0;
    height: 100vh;
    width: 0%;
    background-color: #00000099;
    color: $White;
    z-index: 9999;
    transition: 0.5s;

    i {
        position: absolute;
        top: 0;
        right: 0;
        padding: 2rem;
        transition: 0.5s;

        &:hover {
            color: $PrimaryColor;
        }
    }
}


// navigation bar
nav {
    
    padding: 3rem 0;
    transition: 0.5s;

    ul {
        display: flex;
        margin: 0;
    }
    
    li {
        display: flex;
        align-items: center;
        padding-left: 1.5rem;
        cursor: pointer;
    }

    i {
        font-size: 1.5rem;
    }
    
    #cart_item {
        color: $White;
        transition: 0.5s;

        &:hover {
            color: $PrimaryColor;
        }

    }
    
    #menu_item {
        color: $PrimaryColor;

    }
}

.navbar_active {
    background-color: $Black;
    padding: 1rem 0;

}

// main content

section {
    background-image: url('../assets/image/avadabarbers-homepage-hero-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    
}

#main_header {
    height: 100vh;

    @media (min-width: 1025px) {
        background-image: url('../assets/image/avadabarbers_hero_focalmirror-800x1100.png');
        background-repeat: no-repeat;
        background-position: right;
        background-size: 35rem;
    }
}

h1 {
    font-family: abrilfatface;
    font-size: 5rem;
    color: $White;
}

.divider {
    width: 15rem;
    border-bottom: solid 4px $PrimaryColor;
    margin-top: 0.5rem;
}

p {
    font-size: 1.3rem;
    color: $DarkerGrey;
    margin: 3rem 0;
    line-height: 1;

}

</style>
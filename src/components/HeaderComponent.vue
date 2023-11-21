<template>
    <section>
        <nav class="container fixed-top ">
            Hellossfghjhhgg!
        </nav>
        <div class="container d-flex flex-column justify-content-center align-items-md-baseline align-items-center  " id="main_header">
            <h1>Barber Shop</h1>
            <div class="divider"></div>
            <p>The Pinnacle of Male Grooming</p>
            <div class="btn_primary">learn more</div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'HeaderComponent',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

// navigation bar


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
    font-size: 5rem;
    color: $White;
}

.divider {
    width: 15rem;
    border-bottom: solid 4px $PrimaryColor;
}

p {
    font-size: 1.2rem;
    color: $DarkGrey;
    margin: 2rem 0;
    line-height: 1;

}

</style>
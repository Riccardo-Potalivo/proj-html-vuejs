<template>
    <div class="col-4 p-5">
        <p class="main_description">{{ text }}</p>
        <img :src="'/image/' + img" :alt="user">
        <h6>{{ user }}</h6>

    </div>
</template>

<script>
    export default {
        name: 'ReviewsCard',

        props: {
            text: String,
            img: String,
            user: String
        }
    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

img {
    width: 120px;
    border-radius: 50%;
}

</style>
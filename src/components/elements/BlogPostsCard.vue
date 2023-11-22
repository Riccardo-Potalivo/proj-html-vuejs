<template>
    <div class="col-4 p-3">
        <div class="image_box">
            <img :src="'/image/' + img" :alt="title">
        </div>
        <h4 class="my-4">{{ title }}</h4>
        <p class="main_description">{{ text }}</p>

    </div>
</template>

<script>
    export default {
        name: 'BlogPostsCard',

        props: {
            img: String,
            title: String,
            text: String
        }
    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.image_box {
    width: 100%;
    aspect-ratio: 3 / 2;
    overflow: hidden;
}

img {
    height: 100%;
    width: 100%;
    object-fit: cover;
    transition: 1s;

    &:hover {
        transform: scale(1.1);
        filter: opacity(0.9);
    }
}


</style>
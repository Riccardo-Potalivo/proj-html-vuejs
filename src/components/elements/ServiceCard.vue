<template>
    <div class="col-4 p-5">
        <img :src="'/image/' + img" :alt="title">
        <h4 class="my-4">{{ title }}</h4>
        <p class="main_description">{{ text }}</p>

    </div>
</template>

<script>
    export default {
        name: 'ServiceCard',

        props: {
            img: String,
            title: String,
            text: String
        }
    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

img {
    height: 100px;
}


</style>
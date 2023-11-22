<template>
    <div class="col-3 p-2">
        <img :src="'/image/' + img" :alt="title">
        <h4>{{ title }}</h4>
        <span class="main_description">{{ price }}</span>

    </div>
</template>

<script>
    export default {
        name: 'ProductsCard',

        props: {
            img: String,
            title: String,
            price: String
        }
    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

img {
    width: 100%;
}

span {
    color: $PrimaryColor;
    font-size: 0.7rem;
}


</style>
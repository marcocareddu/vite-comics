<script>
export default {
    props: {
        dcComics: Array,
    },
    data() {
        return {
        }
    }
}

</script>

<template>
    <!-- Cards injected -->
    <div v-for="comic in dcComics" class="col">
        <img :src="comic.thumb" :alt="comic.type">
        <p>{{ comic.series }}</p>
    </div>
</template>

<style scoped>
div {
    flex-basis: calc(100% / 6);
    margin: 20px 0px;
}

img {
    display: block;
    height: 150px;
    width: 150px;
    object-fit: cover;
}

p {
    margin-top: 10px;
    font-size: 0.8rem;
    text-transform: uppercase;
}
</style>
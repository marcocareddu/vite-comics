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
    <div v-for="comic in dcComics" class="col">
        <img :src="comic.thumb" alt="">
        <p>{{ comic.series }}</p>
    </div>
</template>

<style scoped>
img {
    height: 100px;
    width: 100px;
}

p {
    text-transform: uppercase;
}
</style>
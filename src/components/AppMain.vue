<script>
import AppCard from './AppCard.vue';
export default {
    props: {
        dcComics: Array,
    },
    data() {
        return {}
    },
    components: { AppCard }
}
</script>

<template>
    <div class="main-content">

        <!-- Jumbotron -->
        <div class="jumbotron"></div>

        <!-- Main content -->
        <section class="container">
            <div class="row">
                <AppCard :dc-Comics="dcComics" />
            </div>
            <div class="btn-container">
                <button>LOAD MORE</button>
            </div>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixin' as *;
@use '../assets/scss/partials/_customs' as *;

.main-content {
    background-color: $black;
}

.btn-container {
    text-align: center;
    padding-bottom: 20px;
}

button {
    cursor: pointer;
    padding: 10px 50px;
    background-color: $blue;
    color: white;
    font-weight: 600;
    font-size: 0.8rem;
    border: none;
}

.jumbotron {
    height: 300px;
    background-image: url(/src/assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}

.row {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

section {
    height: 100%;
    color: white;
}
</style>
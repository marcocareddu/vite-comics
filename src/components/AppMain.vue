<script>
import AppCard from './AppCard.vue';
export default {
    data() {
        return {}
    },
    components: { AppCard }
}
</script>

<template>
    <div class="main-content">

        <div class="jumbotron"></div>
        <!-- Main content -->
        <section class="container">
            <div class="row">
                <AppCard />
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

.jumbotron {
    height: 300px;
    background-image: url(/src/assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}

.col {
    flex-basis: calc(100% / 6);
}

.row {
    display: flex;
    flex-wrap: wrap;
}

section {
    height: 400px;
    color: white;
}
</style>
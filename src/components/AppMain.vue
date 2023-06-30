<script>
export default {
    data() {
        return {}
    }
}
</script>

<template>
    <div class="main-content">
        <div class="jumbotron"></div>
        <!-- Main content -->
        <section class="container">
            <h1> Content goes here </h1>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixin' as *;
@use '../assets/scss/partials/_customs' as *;

.main-content {
    height: auto;
    background-color: $black;
}

.jumbotron {
    height: 300px;
    background-image: url(/src/assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}

section {
    height: 100%;
    @include flex-between;
    color: white;
}
</style>
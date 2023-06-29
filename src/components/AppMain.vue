<script>
export default {
    data() {
        return {}
    }
}
</script>

<template>
    <div class="main-content">

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
    height: 100px;
    background-color: $black;
}

section {
    height: 100%;
    @include flex-between;
    color: white;
}
</style>
<script>
export default {
    props: {
        navElements: Array
    },
}
</script>

<template>
    <header>
        <div class="container">
            <!-- Logo -->
            <div class="logo">
                <img class="img-fluid" src="@/assets/img/dc-logo.png" alt="Logo DC Comics">
            </div>

            <!-- Navbar -->
            <nav>
                <ul>
                    <li v-for="element in navElements" :key="element.text"><a :href="element.url">{{ element.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixin' as *;
@use '../assets/scss/partials/_customs' as *;

header {
    height: 100px;
    background-color: #fff;

    div {
        height: 100%;
        @include flex-between;
    }

    img {
        height: 80px
    }
}

a {
    font-weight: 600;
    color: $grey;
}
</style>

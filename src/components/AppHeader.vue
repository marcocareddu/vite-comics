<script>
export default {
    data() {
        return {
            navElements: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ],
        }
    }
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
</style>

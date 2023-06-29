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
        <!-- Logo -->
        <div class="logo">
            <img src="@/assets/img/dc-logo.png" alt="Logo DC Comics">
        </div>

        <!-- Navbar -->
        <nav>
            <ul v-for="element in navElements" :key="element.text">
                <li><a :href="element.url">{{ element.text }}</a></li>
            </ul>
        </nav>
    </header>
</template>

<style></style>
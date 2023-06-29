<script>
export default {
    data() {
        return {
            blueMenu: [
                {
                    text: "DIGITAL COMICS",
                    picture: "buy-comics-digital-comics.png"
                },
                {
                    text: "DC MERCHANDISE",
                    picture: "buy-comics-merchandise.png"
                },
                {
                    text: "SUBSCRIPTION",
                    picture: "buy-comics-subscriptions.png"
                },
                {
                    text: "COMICS SHOP LOCATOR",
                    picture: "buy-comics-shop-locator.png"
                },
                {
                    text: "DC POWER EXTRA",
                    picture: "buy-dc-power-visa.svg"
                }
            ]
        }
    },
    methods: {

        // Create picture URL
        createImgUrl(name) {
            return `/src/assets/img/${name}`
        }
    }
}
</script>

<template>
    <!-- Blue band Section -->
    <div class="blue-section">
        <section class="container">
            <ul>
                <li v-for="item in blueMenu" :key="item.text">
                    <a href="#"><img :src="createImgUrl(item.picture)" alt="item.text"><span>{{ item.text }}</span></a>
                </li>
            </ul>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixin' as *;
@use '../assets/scss/partials/_customs' as *;

.blue-section {
    height: 120px;
    background-color: $blue;
}

section {
    height: 100%;
    @include flex-center;
    display: flex;

    ul li {
        padding: 0 10px;
    }

    img {
        padding: 0 5px;
        height: 50px;
    }

    a {
        color: white;
        display: flex;
        align-items: center;
    }
}
</style>
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
            <ul v-for="item in blueMenu" :key="item.text">
                <li><a href="#"><img :src="createImgUrl(item.picture)" alt="item.text">{{ item.text }}</a></li>
            </ul>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixin' as *;
@use '../assets/scss/partials/_customs' as *;

.blue-section {
    background-color: $blue;
}

section {
    height: 100%;
    @include flex-center;

    ul li {
        @include flex-center;
    }

    ;

    img {
        height: 50px;
    }
}
</style>
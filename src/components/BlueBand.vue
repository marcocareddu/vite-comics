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
    <div>
        <ul v-for="item in blueMenu">
            <li><a href="#"><img :src="createImgUrl(item.picture)" :alt="item.text">{{ item.text }}</a></li>
        </ul>
    </div>
</template>

<style></style>
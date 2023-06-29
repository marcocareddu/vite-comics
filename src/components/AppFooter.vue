<script>
export default {
    data() {
        return {
            socialMenu: [
                {
                    text: "facebook logo",
                    picture: "src/assets/img/footer-facebook.png"
                },
                {
                    text: "twitter logo",
                    picture: "src/assets/img/footer-twitter.png"
                },
                {
                    text: "youtube logo",
                    picture: "src/assets/img/footer-youtube.png"
                },
                {
                    text: "pinterest logo",
                    picture: "src/assets/img/footer-pinterest.png"
                },
                {
                    text: "periscope logo",
                    picture: "src/assets/img/footer-periscope.png"
                }
            ],
            footerMenu: [
                {
                    title: "DC COMICS",
                    link: [
                        {
                            name: "Characters",
                            url: "#"
                        },
                        {
                            name: "Comics",
                            url: "#"
                        },
                        {
                            name: "Movies",
                            url: "#"
                        },
                        {
                            name: "TV",
                            url: "#"
                        },
                        {
                            name: "Games",
                            url: "#"
                        },
                        {
                            name: "Videos",
                            url: "#"
                        },
                        {
                            name: "News",
                            url: "#"
                        }
                    ]
                },
                {
                    title: "SHOP",
                    link: [
                        {
                            name: "Shop DC",
                            url: "#"
                        },
                        {
                            name: "Shop DC Collectibles",
                            url: "#"
                        },
                    ]
                },
                {
                    title: "DC",
                    link: [
                        {
                            name: "Terms Of Use",
                            url: "#"
                        },
                        {
                            name: "Privacy policy (New)",
                            url: "#"
                        },
                        {
                            name: "Ad Choices",
                            url: "#"
                        },
                        {
                            name: "Advertising",
                            url: "#"
                        },
                        {
                            name: "Jobs",
                            url: "#"
                        },
                        {
                            name: "Subscritions",
                            url: "#"
                        },
                        {
                            name: "Talent Workshops",
                            url: "#"
                        },
                        {
                            name: "CPSC Certificates",
                            url: "#"
                        },
                        {
                            name: "Ratings",
                            url: "#"
                        },
                        {
                            name: "Shop Help",
                            url: "#"
                        },
                        {
                            name: "Contact Us",
                            url: "#"
                        },
                    ]
                },
                {
                    title: "SITES",
                    link: [
                        {
                            name: "DC",
                            url: "#"
                        },
                        {
                            name: "MAD Magazine",
                            url: "#"
                        },
                        {
                            name: "DC Kids",
                            url: "#"
                        },
                        {
                            name: "DC Universe",
                            url: "#"
                        },
                        {
                            name: "DC Power Visa",
                            url: "#"
                        },
                    ]
                },

            ],
        }
    }
}
</script>

<template>
    <footer>
        <div class="uppper-foot">

            <!-- Menu link -->
            <div v-for="item in footerMenu">
                <h1>{{ item.title }}</h1>
                <ul>
                    <li v-for="link in item.link"><a href="#">{{ link.name }}</a></li>
                </ul>
            </div>
        </div>

        <div class="lower-foot">
            <div class="container">
                <!-- Sign-up -->
                <div>
                    <button>SIGN-UP NOW!</button>
                </div>

                <!-- Social -->
                <div class="social-menu">
                    <div>FOLLOW US</div>
                    <div class="social-icons">
                        <ul v-for="social in socialMenu" :key="social.text">
                            <li><a href="#"><img :src="social.picture" :alt="social.text"></a></li>
                        </ul>
                    </div>
                </div>
            </div>

        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixin' as *;
@use '../assets/scss/partials/_customs' as *;

footer {
    height: 500px;
    background-image: url(../assets/img/footer-bg.jpg);
}

.container {
    height: 100%;
    @include flex-between;
}

.upper-foot {
    height: 100%;
    display: flex;
    flex-direction: column;
}

ul {
    display: flex;
    flex-direction: column;
}

.lower-foot {
    background-color: $grey;
    height: 100px;
}

.social-menu {
    @include flex-between;

    div {
        color: $blue;
    }
}

.social-icons {
    display: flex;
}

button {
    color: white;
    padding: 15px;
    background-color: $grey;
    border: 2px solid $blue;
}
</style>
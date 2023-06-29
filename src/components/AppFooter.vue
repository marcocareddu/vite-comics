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
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="uppper-foot">

            <!-- Menu link -->
            <div>
                <h1>DC COMICS</h1>
                <ul>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                </ul>
                <h1>SHOP</h1>
                <ul>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                </ul>
            </div>
            <div>
                <h1>DC COMICS</h1>
                <ul>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                </ul>
            </div>
            <div>
                <h1>DC COMICS</h1>
                <ul>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                    <li><a href="#">link</a></li>
                </ul>
            </div>
        </div>

        <div class="lower-foot">

            <!-- Sign-up -->
            <div>
                <button>SIGN-UP NOW!</button>
            </div>

            <!-- Social -->
            <div>
                <div>FOLLOW US</div>
                <div>
                    <ul v-for="social in socialMenu" :key="social.text">
                        <li><a href="#"><img :src="social.picture" :alt="social.text"></a></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style></style>
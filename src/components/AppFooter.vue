<script>
export default {
    props: {
        socialMenu: Array,
        footerMenu: Array,
    },
}
</script>

<template>
    <footer>
        <div class="uppper-foot container">

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
    justify-content: flex-start;
}

h1 {
    color: white;
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
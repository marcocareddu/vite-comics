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

        <!-- Upper Footer -->
        <div class="upper-foot container">

            <!-- Menu link -->
            <div v-for="element in footerMenu">
                <div v-for="item in element" class="menu-col">
                    <h1>{{ item.title }}</h1>
                    <ul>
                        <li v-for="link in item.link"><a href="#">{{ link.name }}</a></li>
                    </ul>
                </div>
            </div>

            <div class="big-logo">
            </div>
        </div>


        <!-- Lower Footer -->
        <div class="lower-foot">
            <div class="container">

                <!-- Sign-up -->
                <div>
                    <button>SIGN-UP NOW!</button>
                </div>

                <!-- Social -->
                <div class="social-menu">
                    <div class="signup">FOLLOW US</div>
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
    background-image: url(../assets/img/footer-bg.jpg);
}

// Upper Footer
.upper-foot {
    height: 100%;
    display: flex;

    ul {
        display: flex;
        flex-direction: column;

        li {
            padding: 0px;
        }
    }
}

.menu-col {
    padding-right: 40px;
}

h1 {
    color: white;
    font-size: 1.2rem;
    padding: 10px 0px 5px 0px;
}

a {
    font-size: 0.8rem;
    color: $lightgrey;
}

// Big Logo
.big-logo {
    height: 300px;
    width: 400px;
    background-image: url(../assets/img/dc-logo-bg.png);
    background-repeat: no-repeat;
    background-size: 100%;
    background-position: center;
}

// Lower Footer
.lower-foot {
    background-color: $grey;
    height: 100px;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
    }

    ul {
        display: flex;
        flex-direction: column;

        li {
            padding: 6px;
        }
    }
}


// Socials
.social-menu {
    @include flex-between;

    div {
        color: $blue;
    }
}

.social-icons {
    display: flex;
}

// Button
button {
    font-size: 1.0rem;
    color: white;
    padding: 15px;
    background-color: $grey;
    border: 2px solid $blue;
    font-weight: 600;
    cursor: pointer;
}

.signup {
    font-size: 1.2rem;
    font-weight: 600;
    padding-right: 30px;
}
</style>
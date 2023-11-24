<script>
import AppContact from './AppContact.vue';

export default {
    data() {
        return {
            homeLinks: [
                "Characters",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Videos",
                "News",
            ],
            shopLinks: [
                "Shop DC",
                "Shop DC Collectibles"
            ],
            dcLinks: [
                "Terms Of Use",
                "Privacy policy (New)",
                "Ad Choices",
                "Advertising",
                "Jobs",
                "Subscriptions",
                "Talent Workshops",
                "CPSC Certificates",
                "Ratings",
                "Shop Help",
                "Contact Us"
            ],
            siteLinks: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa"
            ]
        };
    },
    components: { AppContact }
}
</script>

<template>
    <div class="footer-nav">
        <div class="container">
            <div class="footer-content">
                <div class="nav">
                    <div class="left-nav">
                        <div class="home">
                            <h3>DC COMICS</h3>
                            <ul>
                                <li v-for="hlink in homeLinks"><a href="">{{ hlink }}</a></li>
                            </ul>
                        </div>
                        <div class="shop">
                            <h3>SHOP</h3>
                            <ul>
                                <li v-for="sLink in shopLinks"><a href="">{{ sLink }}</a></li>
                            </ul>
                        </div>
                    </div>
                    <div class="right-nav">
                        <div class="about-us">
                            <h3>DC</h3>
                            <ul>
                                <li v-for="dcLink in dcLinks"><a href="">{{ dcLink }}</a></li>
                            </ul>
                        </div>
                        <div class="sites">
                            <h3>SITES</h3>
                            <ul>
                                <li v-for="site in siteLinks"><a href="">{{ site }}</a></li>
                            </ul>
                        </div>
                    </div>

                </div>
                
                <div class="bg-logo"></div>
            </div>
            
        </div>
        
    </div>
    <div class="footer-bottom">
        <div class="container">
            <div class="button">
                <a href="">SIGN-UP NOW!</a>
            </div>
            <AppContact />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.footer-nav {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
    min-height: 200px;   
}

.bg-logo {
    background-image: url('../assets/img/dc-logo-bg.png');
    background-size: contain;
    width: 300px;
    height: 300px
}

.footer-content {
    @include flex(row, space-between, flex-start);
}

.nav {
    @include flex();
    gap: 1.5rem;
    padding-top: 2rem
}

.left-nav {
    @include flex(column, start, start);
    
    .home {
        padding-bottom: 20px
    }
}

.right-nav {
    @include flex(row, center, start);
    gap: 1.5rem;
    padding-bottom: 20px
}

h3 {
    color: white;
    margin-bottom: 1rem;
}

ul {
    list-style-type: none;
    li {
        a {
            text-decoration: none;
            color: rgb(85, 84, 84);
        }
    }
}

.footer-bottom {
    background-color: #303030;
    .container {
        @include flex(row, space-between, center);
        .button {
            border: 4px solid $primaryColor;
            padding: 1rem;
            a {
                text-align: center;
                text-decoration: none;
                display: inline-block;
                color: white;
            }
        }
    }
}

</style>
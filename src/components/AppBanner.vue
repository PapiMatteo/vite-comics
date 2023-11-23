<script>
export default {
    data() {
        return {
            listItems: [
                {
                    img: 'buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS'
                },
                {
                    img: 'buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE'
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    text: 'SUBSCRIPTION'
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    text: 'DC POWER VISA'
                }
            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="banner">
        <div class="small-container">
            <ul>
                <li v-for="item in listItems" :key="item.text"><a href=""><img :src="getImagePath(item.img)" alt="">{{ item.text }}</a></li>
            </ul>
        </div>
    </div>
    
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

.banner {
    min-height: 150px;
    background-color: $primaryColor;
}
.small-container {
    width: 70%;
    margin: 0 auto;
}

ul {
    @include flex(row, space-between);
    padding-top: 2rem;
    list-style-type: none;
    gap: 1rem;
 
    a {
        @include flex(row, space-between);
        gap: .5rem;
        color: white;
        text-decoration: none;
        img {
            width: 50px;
        }
    }
    
}

</style>
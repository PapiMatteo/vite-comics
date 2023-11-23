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
                    text: 'SUBSCRIPTION'
                },
                {
                    img: 'buy-comics-comics-subscription.png',
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    text: 'DC POWER VISA'
                }
            ]
        }
    }
}
</script>

<template>
    <div class="banner">
        <div class="small-container">
            <ul>
                <li v-for="item in listItems" :key="item.text"><img :src="`../assets/img/${item.img}`" alt=""><a href="">{{ item.text }}</a></li>
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
        color: white;
    }
    
}

</style>
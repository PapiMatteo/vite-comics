<script>
import { isReactive } from 'vue';

export default {
    data() {
        return {
            navItems: [
                {
                    text: 'CHARACTERS'
                },
                {
                    text: 'COMICS'
                },
                {
                    text: 'MOVIES'
                },
                {
                    text: 'TV'
                },
                {
                    text: 'GAMES'
                },
                {
                    text: 'COLLECTIBLES'
                },
                {
                    text: 'VIDEO'
                },
                {
                    text: 'FANS'
                },
                {
                    text: 'NEWS'
                },
                {
                    text: 'SHOP'
                }
            ]
        }
    }
}
</script>

<template>
    
    <header class="header">
        <div class="header-top"></div>
        <div class="container">
            <img src="../assets/img/dc-logo.png" alt="Logo DC Comics">

            <ul>
                <li v-for="item in navItems" :key="item.text"><a href="">{{ item.text }}</a></li>
            </ul>
        </div>
    </header>

</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.header {
    height: 130px;
    &-top {
        background-color: #1c1c1c;
        height: 30px;
    }
    img {
        width: 80px;
    }
}

.container {
    padding-top: 10px;
    @include flex(row, space-between, center)
}

ul {
    @include flex(row, space-between, stretch);
    list-style: none;
    gap: 1.2rem;

    a {
        text-decoration: none;
        color: black;
    }

    li {
        &:hover{
            a {
                color: $primaryColor;
                border-bottom: 5px solid $primaryColor;
                padding-bottom: 36px;
            }
        }
    }
    
}

.active {
    color: $primaryColor;
    border-bottom: 5px solid $primaryColor;
    padding-bottom: 36px;
}

</style>
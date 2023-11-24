<script>
export default {
    data() {
        return {
           contactList: [
            'footer-facebook.png',
            'footer-periscope.png',
            'footer-pinterest.png',
            'footer-twitter.png',
            'footer-youtube.png',
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
    <div class="right-bot-footer">
        <h3>FOLLOW US</h3>
    
        <ul>
            <li v-for="contact in contactList"><a href=""><img :src="getImagePath(contact)" alt=""></a></li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;
.right-bot-footer {
    padding: 2rem;
    @include flex(row, center, center);
    gap: 1.5rem;
    h3 {
    color: $primaryColor;
    }
    ul{
        @include flex(row, center, center);
        gap: 1.5rem;
        list-style-type: none;
        li {
            a{
                text-decoration: none;
            }
        }
    }
}


</style>
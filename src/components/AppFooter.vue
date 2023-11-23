<script>
export default {

}
</script>

<template>
    <div class="footer-nav">
        <div class="container">
            <div class="footer-content">
                <div class="nav">
                    <div class="left-nav">
                        <div class="home">TESTO</div>
                        <div class="shop">TESTO</div>
                    </div>
                    <div class="right-nav">
                        <div class="about-us">TESTO</div>
                        <div class="sites">TESTO</div>
                    </div>

                </div>
                
                <img src="../assets/img/dc-logo-bg.png" alt="" class="footer-logo">
            </div>
            
        </div>
        
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;

.footer-nav {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: contain;
    min-height: 200px;   
}

.footer-content {
    @include flex(row, space-between, flex-start);
}

.left-nav {
    @include flex(column, start, start)
}



</style>
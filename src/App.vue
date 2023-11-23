<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue'
import AppBanner from './components/AppBanner.vue';


export default {
  components: {
    AppHeader,
    AppContent,
    AppBanner
  },
  data() {
    return {

    }
  }
}
</script>

<template>
  <AppHeader />
  <AppContent />
  <AppBanner />
</template>

<style lang="scss">
@use "./style/general.scss"
</style>

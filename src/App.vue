<script>
import AppHeader from "./components/AppHeader.vue";
import MainContent from "./components/MainContent.vue";
import BannerOptions from "./components/BannerOptions.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    MainContent,
    BannerOptions,
    AppFooter
  }
}
</script>

<template>
<AppHeader />
<MainContent />
<BannerOptions />
<AppFooter />
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>

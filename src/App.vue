<template>
  <div id="app">
    <SiteHeader />
    <MainContent />
    <SiteFooter />
  </div>
</template>

<script>
import SiteHeader from './components/SiteHeader.vue';
import MainContent from './components/MainContent.vue';
import SiteFooter from './components/SiteFooter.vue';

export default {
  components: {
    SiteHeader,
    MainContent,
    SiteFooter,
  },
};
</script>

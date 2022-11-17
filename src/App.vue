<script>
import AppHeader from "./components/AppHeader.vue";
import MainFirst from "./components/MainFirst.vue";
import AppFooter from "./components/AppFooter.vue";


export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    MainFirst
  }
}
</script>


<template>

  <AppHeader />
  <MainFirst />
  <AppFooter />

</template>



<style lang="scss">
@use "./styles/general.scss";
</style>

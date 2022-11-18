<script>
import AppHeader from "./components/AppHeader.vue";
import MainFirst from "./components/MainFirst.vue";
import MainSecond from "./components/MainSecond.vue";
import AppFooter from "./components/AppFooter.vue";


export default {
  components: {
    AppHeader,
    MainFirst,
    MainSecond,
    AppFooter,

  }
}
</script>


<template>

  <AppHeader />
  <MainFirst />
  <MainSecond />
  <AppFooter />

</template>



<style lang="scss">
@use "./styles/general.scss";
</style>

<script>
import AppHeader from "./components/AppHeader.vue";
import MainFirst from "./components/MainFirst.vue";
import MainSecond from "./components/MainSecond.vue";
import MainThird from "./components/MainThird.vue";
import AppFooter from "./components/AppFooter.vue";


export default {
  components: {
    AppHeader,
    MainFirst,
    MainSecond,
    MainThird,
    AppFooter,

  }
}
</script>


<template>

  <AppHeader />
  <MainFirst />
  <MainSecond />
  <MainThird />
  <AppFooter />

</template>



<style lang="scss">
@use "./styles/general.scss";
</style>

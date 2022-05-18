<template>
  <div id="app">
    <!-- Header -->
    <AppHeader />
    <!-- Main -->
    <main>
      <ProductsList />
    </main>

    <!-- Footer -->
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
import ProductsList from "./components/ProductsList.vue";

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    ProductsList
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";



</style>

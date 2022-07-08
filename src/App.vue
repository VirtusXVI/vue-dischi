<template>
  <div id="app">
    <MyHeader/>
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader.vue"
export default {
  name: 'App',
  components: {
    MyHeader,
  }
}
</script>

<style lang="scss">
@import './assets/scss/common.scss';
#app{
  font-family: "Montserrat";
}
</style>
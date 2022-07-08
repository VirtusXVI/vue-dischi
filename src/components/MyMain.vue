<template>
  <div class="main-background">
    <div class="main-container">
        <MusicCard />
    </div>
  </div>
</template>

<script>
import MusicCard from "./MusicCard.vue"
    export default {
        name: "MyMain",
        component:{
            MusicCard,
        }
    }
</script>

<style lang="scss" scoped>
    .main-background{
        background-color: #1e2d3b;
    }
    .main-container{
        width: 70%;
        height: calc(100vh - 60px);
        margin: 0 auto;
    }
</style>
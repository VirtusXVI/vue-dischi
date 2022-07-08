<template>
  <div>
    <div class="header-background">
        <div class="header-container">
            <img src="../assets/img/Spotify.png" alt="">
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "MyHeader"
}
</script>

<style lang="scss" scoped>
    .header-background{
        background-color: #2e3a46;
    }
    .header-container{
        width: 98%;
        margin: 0 auto;
        height: 70px;
        display: flex;
        align-items: center;
    }
    img{
        height: 50px;
    }
</style>
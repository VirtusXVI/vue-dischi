<template>
  <div class="card-1">
    <div class="card">
        <div class="card-image">
            <img :src="cover" alt="Album Cover">
        </div>
        <div class="card-text">
            <h2>{{ title }}</h2>
            <p>{{ author }}</p>
            <p>{{ date }}</p>
        </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "MusicCard",
        props: {
            author: String,
            cover: String,
            title: String,
            date: String
        },
    }
</script>

<style scoped lang="scss">
    .card-1{
        width: calc(90% / 5);
    }
    .card{
        height: calc(100% / 2);
    }
    .card-image{
        width: 100%;
    }
    .card-image img{
        width: 100%;
        object-fit: cover;
        object-position: top;
        aspect-ratio: 1;
    }
    .card-text{
        height: 30%;
        padding: 1rem 0;
        color: grey;
        text-align: center;
    }
</style>
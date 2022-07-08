<template>
  <div>
    <div class="cards-container">
        <div class="card">
            <div class="card-image">
                ciao
            </div>
            <div class="card-text">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque ipsa eveniet, aut vero consequatur numquam recusandae perferendis ducimus molestias, ipsam debitis dicta iusto animi esse quas fugit reiciendis laboriosam temporibus.
            </div>
        </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "MusicCard",
    }
</script>

<style scoped lang="scss">
    .cards-container{
        width: 97%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
    .card{
        width: calc(86% / 6);
        height: calc(100% / 2);
        margin-bottom: 3rem;
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
    }
</style>
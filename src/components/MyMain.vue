<template>
  <div class="main-background">
    <div class="main-container">
        <div class="cards-container">
            <MusicCard :title="musicDatas[index].title" :date="musicDatas[index].year" :author="musicDatas[index].author" :cover="musicDatas[index].poster" v-for="song,index in musicDatas" :key="index"/>
        </div>
    </div>
  </div>
</template>

<script>
    import MusicCard from "./MusicCard.vue"
    import axios from 'axios'
    export default {
        name: "MyMain",
        components:{
            MusicCard,
        },
        data: function () {
            return {
                musicDatas: null
            }        
        },
        methods:{
            generateElements(){
                axios.get("https://flynn.boolean.careers/exercises/api/array/music")
                .then((response) =>{
                        this.musicDatas = response.data.response;
                        console.log(this.musicDatas);
                })
            }
        },
        mounted(){
            this.generateElements();
        }
    }
</script>

<style lang="scss" scoped>
    .main-background{
        background-color: #1e2d3b;
    }
    .main-container{
        width: 70%;
        height: calc(100vh - 70px);
        margin: 0 auto;
    }
    .cards-container{
        width: 97%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        padding-top: 1rem;
    }
</style>
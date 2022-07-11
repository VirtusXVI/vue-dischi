<template>
  <div class="main-background">
    <div class="main-container">
        <MySelect @filter="setActiveGenre"/>
        <div class="cards-container">
            <MusicCard 
            :title="song.title" 
            :date="song.year" 
            :author="song.author" 
            :cover="song.poster" 
            v-for="song,index in filteredSongs"
            :key="index"/>
        </div>
    </div>
  </div>
</template>

<script>
    import MusicCard from "./MusicCard.vue"
    import MySelect from "./MySelect.vue"
    import axios from 'axios'
    export default {
        name: "MyMain",
        components:{
            MusicCard,
            MySelect
        },
        data: function () {
            return {
                musicDatas: null,
                musicGenre: null,
                generes: [],
                activeGenre: "All"
            }        
        },
        computed:{
            filteredSongs(){
                if(this.activeGenre === "All"){
                    return this.musicDatas;
                }
                return this.musicDatas.filter((item) => item.genre === this.activeGenre)
            }
        },
        methods:{
            generateElements(){
                axios.get("https://flynn.boolean.careers/exercises/api/array/music")
                .then((response) =>{
                    this.musicDatas = response.data.response;
                    for(let i = 0; i < this.musicDatas.length;i++){
                        this.generes.push(this.musicDatas)
                    }
                    console.log(this.generes[0]);
                })
            },
            setActiveGenre(genre){
                this.activeGenre = genre;
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
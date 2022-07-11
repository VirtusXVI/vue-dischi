<template>
  <div class="select-alignments">
    <select v-model="musicGenre" name="genre" id="genre">
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
    </select>
    <button @click="$emit('filter', musicGenre)">Filter</button>
  </div>
</template>

<script>
export default {
    name: "MySelect",
    data: function () {
            return {
                musicGenre: null
            }        
        },
}
</script>

<style lang="scss" scoped>
.select-alignments{
    display: flex;
    justify-content: center;
    align-items: center;
}
select{
    margin: 1rem 0;
    padding: 0.2rem 2rem;
    color: white;
    background-color: grey;
    border-radius: 10px;
}
button{
    padding: 0.2rem 1rem;
    color: white;
    background-color: grey;
    border-radius: 10px;
    margin: 0 1rem;
}
</style>


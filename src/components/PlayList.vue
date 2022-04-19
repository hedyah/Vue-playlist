<template>
    <div>
        <h2>PlayList</h2>
        <h4>{{songTitle}}</h4>
        <SongList/>
    </div>
</template>

<script>
import SongList from './SongList.vue'

    export default {
    components: { SongList },
        methods: {
            clickPlay() {
                this.$emit('childClicked', this.songTitle)
                this.$root.$emit('childSong', this.id)
            },
            updateSong(songId){
                if (this.id == songId){
                    this.post = true;
                }else{
                    this.post = false;
                }
            }
        },
        data() {
            return {
                post: true
            }
        },
        mounted (){
            this.$root.$on ('childSong', this.updateSong)
        }
    }
</script>

<style scoped>
*{
    background-color: rgb(67, 148, 214);
}
</style>
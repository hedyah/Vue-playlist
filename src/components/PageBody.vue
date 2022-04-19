<template>
    <div>
        <h2>Pick a Song {{childClicked}}</h2>
        <PlayList v-if="post in posts"
        :key="post.id"
        :songTitle="post.songTitle"
        />
        <SongList v-for="post in posts"
        :key="post.id"
        :songArtist="post.songArtist"
        :songTitle="post.songTitle"
        
        />
    </div>
</template>

<script>
import PlayList from './PlayList.vue'
import SongList from './SongList.vue'

    export default {
    components: { PlayList, SongList },
        name: "PageBody",
        data() {
            return {
                userinput:"",
                posts:[
                    {
                        songArtist: "Shakira",
                        songTitle: "Whenever, Wherever"
                    },
                    {
                        songArtist: "Burna Boy",
                        songTitle: "Ginger"
                    },
                    {
                        songArtist:"SZA",
                        songTitle:"Love Galore"
                    },
                    {
                        songArtist:"FireBoy DML",
                        songTitle: "Peru"
                    },
                    {
                        songArtist:"MEDUZA",
                        songTitle: "Paradise"
                    },
                    {
                        songArtist:"SZA",
                        songTitle:"All The Stars"
                    }
                ]
        }
        
    }
    }
</script>

<style scoped>
*{
    background-color: rgb(43, 137, 140);
    
}
div{
    display: grid;
    grid-template-columns: 2fr 2fr;
    
}
</style>
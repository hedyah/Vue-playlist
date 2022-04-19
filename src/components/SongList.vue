<template>
    <div>
        <h2>{{ songArtist}}</h2>
        <h4>{{ songTitle}}</h4>
    </div>
</template>

<script>
    export default {
        name: "SongList",
        props: {
            songArtist : String,
            songTitle : String
        },
    }
</script>

<style  scoped>
*{
    background-color: rgb(100, 246, 198);
    border: 3px solid darkblue;

    margin: 20px;
}
</style>
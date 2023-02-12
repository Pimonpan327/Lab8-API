<template>
    <div> 
    <h1>Population Memes</h1>
    <button @click="getMemes()">Load Memes</button>
    <ul>
    <li v-for="meme in memes" :key="meme.id">
        {{ meme.id }}{{ meme.name }} {{ meme.url }} 
        {{ meme.height }} {{ meme.width }} {{ meme.box_count }}
    </li>
    </ul>
    </div>
</template>
<script setup>
import axios from"axios";
import { ref } from"vue";
const memes = ref();
const url = ref("https://api.imgflip.com/get_memes");
function getMemes() {
    axios    
    .get(url.value)    
    .then((response) => {
        memes.value = response.data;   
    })    
        .catch((err) => {console.log(err);    
        });
    }
</script>
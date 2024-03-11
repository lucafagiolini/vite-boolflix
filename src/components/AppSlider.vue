<script>

import AppSliderItem from './AppSliderItem.vue';

import { store } from '../store.js';


export default {
    data() {
        return {
            store
        }
    },
    name: 'AppSlider',
    components: {
        AppSliderItem
    }
}

</script>




<template>
    <div>
        <h3 class="container">Movies</h3>
        <ul class=" movie_slider container d-flex justify-content-center align-items-center gap-5 p-0 py-5">
            <h3>Movies and tv </h3>
            <AppSliderItem
            v-for="currentMovie in store.movies"
            :movie="currentMovie"
            >
                
            </AppSliderItem>
        </ul>

        <h3 class="container">Tv Series</h3>
        <ul class=" movie_slider container d-flex justify-content-center align-items-center gap-5 p-0 py-5">
            <h3>Movies and tv </h3>
            <AppSliderItem
            v-for="currentMovie in store.tvseries"
            :movie="currentMovie"
            >
                
            </AppSliderItem>
        </ul>


    </div>



</template>




<style lang="scss">

.movie_slider {
    list-style: none;
   
    width: 100%;
    
    
    overflow-x: auto;
    overflow-y: hidden;
    gap: 5px;
    li {
        flex: 0 0 auto;
        width: 200px;
    }
}

</style>
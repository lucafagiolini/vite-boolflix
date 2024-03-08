<script>
import axios from 'axios';
import { store } from '../store.js';

export default {
    name: 'AppSearchBar',
    data() {
        return {
            store, 
        }
    },
}

</script>








<template>
    <div class="container">
        <input type="text"  placeholder="Search for a movie" />
        <button @click="searchMovies">Search</button>
    </div>
</template>




<style>

</style>

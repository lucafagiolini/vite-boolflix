<script>
import axios from 'axios';
import { store } from '../store.js';

export default {
    name: 'AppSearchBar',
    data() {
        return {
            store,
            searchQuery: '',
        }
    },

    methods: {
        searchMovies() {
            let formattedQuery = this.searchQuery.split(' ').join('+');
            axios.get(`https://api.themoviedb.org/3/search/movie?api_key=c7bfad605bd2ec8fb7088c733fe64d61&query=${formattedQuery}`)
                .then(response => {
                    this.store.movies = response.data.results;
                })
                .catch(error => {
                    console.log(error);
                });

            axios.get(`https://api.themoviedb.org/3/search/tv?api_key=c7bfad605bd2ec8fb7088c733fe64d61&query=${formattedQuery}`)
                .then(response => {
                    this.store.tvseries = response.data.results;
                    console.log(this.store.tvseries);
                })
                .catch(error => {
                    console.log(error);
                });    
        }
    }
}

</script>








<template>
    <div class="d-flex justify-content-between mt-3 ">
        <div>
            <img id="searchflix_logo" src="/src/assets/logo/searchflix_logo.png" alt="">
        </div>
        <div>
            <input type="text" v-model="this.searchQuery"  placeholder="Search for a movie" />
            <button @click="searchMovies">Search</button>
        </div>
    </div>
</template>




<style lang="scss">

#searchflix_logo {
   width: 150px;
}

</style>

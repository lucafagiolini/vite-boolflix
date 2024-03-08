<script>
import { store } from './store.js';
import axios from 'axios';
import AppSearchBar from './components/AppSearchBar.vue';
import AppSlider from './components/AppSlider.vue';

export default {
  name: 'App',
  data () {
    return {
      store
    }
  },
  components: {
    AppSlider,
    AppSearchBar
  },

  created() {
    axios.get('https://api.themoviedb.org/3/movie/top_rated?api_key=c7bfad605bd2ec8fb7088c733fe64d61')
      .then(res => {
          this.store.movies = res.data.results;
      });

    axios.get('https://api.themoviedb.org/3/movie/top_rated?api_key=c7bfad605bd2ec8fb7088c733fe64d61')
      .then(res => {
          this.store.tvseries = res.data.results;
      });}

      
}

</script>

<template>
  <AppSearchBar></AppSearchBar>
  <AppSlider></AppSlider>
</template>


<style>

</style>

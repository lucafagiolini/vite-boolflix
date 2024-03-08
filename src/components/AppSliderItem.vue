<script>
export default {
    name: 'AppSliderItem',
    
    props: {
        movie: Object
    }
}

</script>




<template>

    <li>
        <img class="w-100" tabindex="0" :src="movie && movie.poster_path ? 'https://image.tmdb.org/t/p/w342' + movie.poster_path : 'https://www.innerintegratori.it/wp-content/uploads/2021/06/placeholder-image.png'" alt="">

        <h5>{{ movie.title }}</h5>
   
        <h5> {{ movie.original_title }}</h5>
    
        <span> {{ movie.original_language }}</span>
    
        <span> {{ movie.vote_average }} </span>
    </li>

</template>




<style>

</style>
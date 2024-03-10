<script>
export default {
    name: 'AppSliderItem',
    
    props: {
        movie: Object
    },

    computed: {

    }
}

</script>




<template>

    <li class="card">
        <img class="w-100" tabindex="0" :src="movie && movie.poster_path ? 'https://image.tmdb.org/t/p/w342' + movie.poster_path : 'https://www.innerintegratori.it/wp-content/uploads/2021/06/placeholder-image.png'" alt="">

        <h5>{{ movie.title }}</h5>
   
        <h5> {{ movie.original_title }}</h5>

        <img class="flag" :src="'/src/assets/flags/' + movie.original_language + '.png'" alt="">  

        <span> {{ movie.original_language }}</span> 
    
        <span> {{ movie.vote_average }} </span>
    </li>

</template>




<style>
.card {
    width: 300px;
    object-fit: cover;

    img {
        max-height: 400px;
       
    }

    .flag {
        width: 20px;
        object-fit: cover;
    }

}

</style>
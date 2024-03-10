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

    <li class="card position-relative">
        <img class="w-100" tabindex="0" :src="movie && movie.poster_path ? 'https://image.tmdb.org/t/p/w342' + movie.poster_path : 'https://www.innerintegratori.it/wp-content/uploads/2021/06/placeholder-image.png'" alt="">
        <div id="movie_details" class="position-absolute h-100 w-100">
            <h5>{{ movie.title }}</h5>
       
            <h5> {{ movie.original_title }}</h5>
    
            <img class="flag" :src="'/src/assets/flags/' + movie.original_language + '.png'" alt="">  
    
            <span> {{ movie.original_language }}</span> 
        
            <span> {{ movie.vote_average }} </span>
        </div>
    </li>

</template>




<style lang="scss">
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

    #movie_details {
        display: none;
        
    }

    &:hover {

        .card {
            transform: scale(1.1);
            transition: transform 0.5s;
            
        }

        #movie_details {
            display: flex;
            flex-direction: column;
            background-color: rgba(0, 0, 0, 0.887);
        }
    }

}

</style>
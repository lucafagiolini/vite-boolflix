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

    <li class="card position-relative rounded-3">
        <img class="w-100 rounded-3" tabindex="0" :src="movie && movie.poster_path ? 'https://image.tmdb.org/t/p/w342' + movie.poster_path : 'https://www.innerintegratori.it/wp-content/uploads/2021/06/placeholder-image.png'" alt="">
        <div id="movie_details" class="position-absolute h-100 w-100 justify-content-end p-2 rounded-3">
            <h5>Title: {{ movie.title }}</h5>
       
            <h5>Original title: {{ movie.original_title }}</h5>
    
            <img class="flag" :src="'/src/assets/flags/' + movie.original_language + '.png'" alt="">  
    
            <span>Original language: {{ movie.original_language }}</span> 
        
            <span>Vote: {{ movie.vote_average }} </span>
        </div>
    </li>

</template>




<style lang="scss">
.card {
    width: 250px;
    object-fit: cover;
    cursor: pointer;
    border: none;
    

    &:hover {
        transform: scale(1.1);
        transition: transform 0.3s;

        box-shadow: #e50913 0px 0px 15px; 
        
    }
   
    

    .flag {
        width: 20px;
        object-fit: cover;
    }

    #movie_details {
        display: none;
        
    }

    &:hover {

        #movie_details {
            display: flex;
            flex-direction: column;
            background-color: #222528e7;
            
            box-shadow: #e50913 0px 0px 15px; 
        }
    }

}

</style>
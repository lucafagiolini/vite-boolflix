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
        <h5>{{ movie.title }}</h5>
   
        <h5> {{ movie.original_title }}</h5>
    
        <span> {{ movie.original_language }}</span>
    
        <span> {{ movie.vote_average }} </span>
    </li>



</template>




<style>

</style>
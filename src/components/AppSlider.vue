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
        <ul class=" container d-flex flex-wrap gap-5 my-5 p-0">
            <AppSliderItem
            v-for="currentMovie in store.movies"
            :movie="currentMovie"
            >
                
            </AppSliderItem>
        </ul>
    </div>



</template>




<style>

</style>
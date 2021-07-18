<template>

    <div >
        <div class="row">
            <movieCards :movie="movie" v-for="movie in movies" :key="movie.id" ></movieCards>
        </div>
        
    </div>

</template>

<script>

import movieCards from './movieCards'
import Vuex from 'vuex'

export default {
    components: {
        movieCards
    },
    computed: {
        ...Vuex.mapGetters({
            movies: 'filteredMovies'
        }) 
    }
}

</script>
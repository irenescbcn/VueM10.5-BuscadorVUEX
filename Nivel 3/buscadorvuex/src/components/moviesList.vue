<template>

    <div >
        <div class="row " v-if="movies.length > 0">
            <movieCards :movie="movie" v-for="movie in movies" :key="movie.id" ></movieCards>
        </div>
        <div v-else-if="1" class="alert alert-danger mt-2">No hay películas disponibles</div>
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
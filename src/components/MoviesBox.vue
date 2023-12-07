<template>

    <div class="grid">     

        <div v-for="movie of movies" :key="movie.movie_id" >

            <SingleMovie :movie=movie />

        </div>
    </div>    

</template>

<script>

import SingleMovie from './SingleMovie.vue'

export default{

    name:'MoviesBox',

    props:{

        movies: Array

    },

    components:{

        SingleMovie

    }

}

</script>

<style scoped>

div{

    text-align: center;

}
.grid{
    display : grid;
    grid-template-columns: auto;
}

</style>
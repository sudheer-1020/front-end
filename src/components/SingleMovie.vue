<template>

    <div :class="movie.movie_is_released ? 'green' :'red' ">
            <h1>{{movie.movie_name}}</h1>
            <div class="flex" >
              <h2>{{movie.movie_year}} </h2>
            </div>
            <h2 class="flex">{{movie.movie_runtime}}</h2>
            <h2 class ="genre">{{movie.movie_genre}}</h2>


           <h2 class="language">{{movie.movie_language}}</h2>

           <h2 class="flex">{{movie.movie_rating}}</h2>

           <h2 class="flex">{{movie.movie_director}}</h2>
    </div>

</template>

<script>
export default {

    name: 'SingleMovie',

    props:{

        movie: Array

    }
}

</script>
<style scoped>

.green{

  background-color: green;

}

h2{

    font-size: 1em;

}

h4{

  margin: 2px

}

div{

  

  color: black;

  padding: 1em;

  text-align: center;

  margin: 1em;
  width: 60%;
  margin-left:20%;
  border: 1px solid transparent;
  border-radius: 10px;

}
.red{

  background-color: orangered !important;

}

.genre,.language,.flex{
  border:1px solid black;
  padding: 7px;
  border-radius: 10px;
  width:25%;
  margin:5px auto;
}

</style>







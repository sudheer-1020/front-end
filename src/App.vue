<template>
   <div>
    <MoviesHeader />
   <MoviesBox :movies=movies />
   </div>

</template>

<script>
import MoviesBox from './components/MoviesBox.vue'
import MoviesHeader from './components/MoviesHeader.vue'

export default{
  name: 'App',
  components:{
    MoviesBox,
    MoviesHeader

  },
  data(){
    return {
      movies: []
    }
  },
  methods:{
    //promises
    async fetchMovies(){
      const res = await fetch(" https://movies-g9w3.onrender.com/api ");
      const data = await res.json()
      console.log(data)
      return data[0].movieshub
    }
  },
  async created(){
    this.movies = await this.fetchMovies();
  }
  

}


</script>

<style>
</style>
<template>
  <div>
    <div class="search">
      <input v-model="title" placeholder="Pesquise por um titulo">
      <button type="button" @click="getMovies()">Pesquisar</button>
    </div>
    <div class="movies">
      <div class="movie" v-for="filme in movies" :key="filme.id">
        <img :src="filme.Poster" width="100px">
        <h5> {{filme.Title}} </h5>
        <h5> {{filme.Year}} </h5>
      </div>
    </div>
</div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'Home',
  data() {
    return {
      title: '',
      movies: [],
    };
  },
  created() {
    this.getMovies();
  },
  methods: {
    getMovies() {
      const { title } = this;
      const url = `http://www.omdbapi.com/?s=${title}&page=1&apikey=92370e9f`;

      fetch(url)
        .then((response) => response.json())
        .then((response) => {
          this.movies = response.Search;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>
<style>
  .search {
    margin: 10px;
    text-align: center;
  }

  button {
    background: #222;
    color: var(--color-light);
    border-radius: 3px;
  }

  input {
    border: solid 1px;
    border-radius: 3px;
  }

  .movies {
    margin: 30px;
    display: flex;
    flex-wrap: wrap;
  }

  .movie {
    width: 100px;
    margin: 10px;
  }

</style>

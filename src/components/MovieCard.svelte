<script>
  export let movie
</script>

<div class="movie-card">
  <a href={'/movie/' + movie.id}>
    <img
      src={`https://image.tmdb.org/t/p/w500${movie.poster_path}`}
      alt={movie.title}
    />
  </a>
  <div class="description">
    <h2>{movie.title}</h2>
    <p>{movie.release_date}</p>
  </div>
</div>

<style>
  img {
    width: 100%;
    border-top-left-radius: 0.5rem;
    border-top-right-radius: 0.5rem;
  }
  h2 {
    font-size: 0.9rem;
  }
  .description {
    padding: 0 1rem;
  }
  p {
    font-size: 0.7rem;
  }
  .movie-card {
    box-shadow: 0.1rem 0.05rem 0.4rem 0.1rem rgba(0, 0, 0, 0.1);
    border-radius: 0.5rem;
  }
</style>

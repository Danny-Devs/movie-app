<script context="module">
  export async function load({ fetch }) {
    const res = await fetch(
      'https://api.themoviedb.org/3/movie/popular?api_key=abc357e83b8a6afc8966b884f5be4202&language=en-US&page=1'
    )
    const data = await res.json()
    console.log(data)
    if (res.ok) {
      return {
        props: { popular: data.results },
      }
    }
  }
</script>

<script>
  import PopularMovies from '../components/PopularMovies.svelte'
  export let popular
</script>

<section>
  <PopularMovies {popular} />
</section>

<style>
</style>

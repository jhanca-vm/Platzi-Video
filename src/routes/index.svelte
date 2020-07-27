<script context="module">
  export async function preload() {
    let urlApi = 'https://api.themoviedb.org/3/trending';
    let apiKey = '286f7dc0581d1b8e193af99f770c7cba';

    const resTrending = await this.fetch(`${urlApi}/all/day?api_key=${apiKey}&language=es`);
    const resMovies = await this.fetch(`${urlApi}/movie/week?api_key=${apiKey}&language=es`);
    const resTv = await this.fetch(`${urlApi}/tv/week?api_key=${apiKey}&language=es`);
    const trending = await resTrending.json();
    const movies = await resMovies.json();
    const series = await resTv.json();

    return {
      trending: trending.results,
      movies: movies.results,
      series: series.results,
    };
  }
</script>

<script>
  import Search from '../components/Search.svelte';
  import Carousel from '../components/Carousel.svelte';

  export let trending;
  export let movies;
  export let series;
</script>

<svelte:head>
  <title>Platzi Video</title>
</svelte:head>

<Search />
<Carousel name="Tendencias" data={trending} />
<Carousel name="Películas" data={movies} />
<Carousel name="Series" data={series} />

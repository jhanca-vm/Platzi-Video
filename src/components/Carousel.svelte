<script>
  export let name;
  export let data;
</script>

<style>
  section {
    overflow: scroll;
    scrollbar-width: none;
  }

  section::-webkit-scrollbar {
    display: none;
  }

  img {
    width: 100%;
    object-fit: cover;
  }

  h6 {
    margin-top: 0.5rem;
    font-size: 12px;
  }

  p {
    font-size: 10px;
    margin: 3px 0px;
  }

  .carousel {
    font-size: 0;
    white-space: nowrap;
    margin: 32px 0px;
    padding-bottom: 10px;
    transition: 450ms transform;
  }

  .item {
    width: 120px;
    height: 180px;
    display: inline-block;
    margin-right: 10px;
    font-size: 20px;
    border-radius: 20px;
    position: relative;
    overflow: hidden;
    cursor: pointer;
    transition: 450ms all;
    transform-origin: center left;
  }

  .item:last-of-type {
    margin-right: 0;
  }

  .carousel:hover .item {
    opacity: 0.3;
  }

  .carousel:hover .item:hover {
    opacity: 1;
    transform: scale(1.25);
  }

  .item:hover ~ .item {
    transform: translate3d(30px, 0, 0);
  }

  .item--detail {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-end;
    padding: 10px;
    font-size: 10px;
    white-space: normal;
    background: linear-gradient(to top, rgba(0, 0, 0, 0.9) 0%, rgba(0, 0, 0, 0) 100%);
    opacity: 0;
    transition: 450ms opacity;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }

  .item:hover .item--detail {
    opacity: 1;
  }

  @media (min-width: 768px) {
    .carousel {
      margin: 45px 0;
    }

    .item {
      width: 180px;
      height: 270px;
    }

    .item:hover ~ .item {
      transform: translate3d(45px, 0, 0);
    }
  }
</style>

<h3>{name}</h3>
<section>
  <div class="carousel">
    {#each data as item}
      {#if item.media_type === 'movie'}
        <div class="item">
          <img src={`https://image.tmdb.org/t/p/w500${item.poster_path}`} alt={item.title} />
          <div class="item--detail">
            <h6>{item.title}</h6>
            <p>{item.vote_average}</p>
          </div>
        </div>
      {:else if item.media_type === 'tv'}
        <div class="item">
          <img src={`https://image.tmdb.org/t/p/w500${item.poster_path}`} alt={item.name} />
          <div class="item--detail">
            <h6>{item.name}</h6>
            <p>{item.vote_average}</p>
          </div>
        </div>
      {/if}
    {/each}
  </div>
</section>

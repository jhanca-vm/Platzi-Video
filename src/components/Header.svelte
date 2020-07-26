<script>
  export let segment;
</script>

<style>
  header {
    height: 70px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 1rem;
    background: #272343;
    color: white;
  }

  .logo {
    width: 120px;
  }

  ul {
    display: flex;
    list-style: none;
  }

  li {
    margin-left: 1rem;
    font-size: 12px;
    font-weight: 600;
  }

  @media (min-width: 768px) {
    header {
      height: 100px;
      padding: 0 1.25rem;
    }

    .logo {
      width: 200px;
    }

    li {
      margin-left: 1.5rem;
      font-size: 16px;
    }
  }

  @media (min-width: 1024px) {
    header {
      padding: 0 2rem;
    }
  }
</style>

<header>
  <a rel="prefetch" href=".">
    <img class="logo" src="logo-platzi-video.png" alt="Platzi Video" />
  </a>
  {#if segment != 'iniciar-sesion' && segment != 'registro'}
    <nav>
      <ul>
        <li>
          <a href="iniciar-sesion">Iniciar Sesión</a>
        </li>
        <li>
          <a href="registro">Regístrate</a>
        </li>
      </ul>
    </nav>
  {/if}
</header>

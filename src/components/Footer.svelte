<script>
  export let segment;
</script>

<style>
  footer {
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 14px;
    background-color: #272343;
  }

  .bg-light {
    background-color: #bae8e8;
    color: #272343;
  }
</style>

<footer class:bg-light={segment === 'iniciar-sesion' || segment === 'registro'}>
  Powered by @jhanca-vm
</footer>

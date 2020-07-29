<style>
  section {
    min-height: calc(100vh - 160px);
    padding: 1rem;
    font-size: 14px;
  }

  h2 {
    text-align: center;
  }

  form {
    display: flex;
    flex-direction: column;
  }

  form > input {
    height: 50px;
    margin-bottom: 20px;
    padding: 0px 20px;
    font-size: 16px;
    outline: none;
    border: none;
    border-bottom: 2px solid white;
    background-color: transparent;
  }

  input::placeholder {
    color: inherit;
  }

  button {
    height: 50px;
    margin: 10px 0px;
    font-size: 16px;
    font-weight: bold;
    letter-spacing: 1px;
    background-color: rgba(255, 255, 255, 0.3);
    border-radius: 25px;
    border: none;
    cursor: pointer;
  }

  p {
    font-size: 14px;
    color: #272343;
  }

  p a {
    font-weight: 700;
    color: inherit;
  }

  a:hover {
    text-decoration: underline;
  }

  i {
    margin-right: 0.25rem;
  }

  .container {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    min-height: 500px;
  }

  .remember-me {
    display: flex;
    justify-content: space-between;
    margin-top: 10px;
  }

  .social-media > div {
    align-items: center;
    display: flex;
    margin-bottom: 10px;
  }

  @media (min-width: 568px) {
    .container {
      height: 600px;
      width: 400px;
      margin: 1rem auto;
      padding: 50px 50px 40px;
      border: 2px solid white;
      border-radius: 40px;
      background-color: rg0px 30pxba (255, 255, 255, 0.1);
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.25), 0 8px 10px rgba(0, 0, 0, 0.22);
    }
  }
</style>

<section>
  <div class="container">
    <h2>Iniciar sesión</h2>
    <form on:submit|preventDefault>
      <input type="text" placeholder="Correo" />
      <input type="password" placeholder="Contraseña" />
      <button>Iniciar sesión</button>
      <div class="remember-me">
        <label>
          <input type="checkbox" />
          Recuérdame
        </label>
        <a href="/">Olvidé mi contraseña</a>
      </div>
    </form>
    <div class="social-media">
      <div>
        <i class="fab fa-google" />
        Inicia sesión con Google
      </div>
      <div>
        <i class="fab fa-twitter" />
        Inicia sesión con Twitter
      </div>
    </div>
    <p>
      ¿No tienes cuenta?
      <a href="registro">Regístrate</a>
    </p>
  </div>
</section>

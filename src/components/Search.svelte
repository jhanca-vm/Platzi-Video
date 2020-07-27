<style>
  section {
    height: 150px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    margin-bottom: 1.5rem;
  }

  h2 {
    font-size: 1.5rem;
  }

  input {
    width: 80%;
    height: 40px;
    max-width: 420px;
    margin-top: 20px;
    padding: 0px 20px;
    font-size: 16px;
    border: 2px solid white;
    border-radius: 25px;
    background-color: rgba(255, 255, 255, 0.1);
  }

  input::placeholder {
    color: white;
    opacity: 0.5;
  }

  @media (min-width: 1024px) {
    section {
      height: 180px;
    }

    h2 {
      font-size: 2rem;
    }

    input {
      max-width: 600px;
    }
  }
</style>

<section>
  <h2>¿Qué quieres ver hoy?</h2>
  <input type="text" placeholder="Buscar..." />
</section>

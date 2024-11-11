<script>
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="contact">
    <RouterLink :to="{name: 'home'}"> Inicio </RouterLink>
    <h1>Contáctate Con Nosotros</h1>

    <form class="mt-5">
      <div class="mb-3">
        <label id="email" class="form-label">Tu Email</label>
        <input type="email" class="form-control" id="email" aria-describedby="emailHelp">
      </div>
      <div class="mb-3">
        <label for="comentario" class="form-label">Comentario</label>
        <textarea class="form-control p-3" id="comentario"></textarea>
      </div>
      <button type="submit" class="btn fw-bold px-4 ms-auto d-block btn-info text-white">Contactar</button>
    </form>
  </div>
</template>

<style>

.contact {
  margin: 8rem 2rem;
  min-height: 50vh;
}

h1 {
  text-align: center;
}

form {
  max-width: 40rem;
  margin-inline: auto;
}

</style>

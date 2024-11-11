<script>
import { RouterLink } from "vue-router";

export default {
  name: "TheNavbar",
};
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-light fixed-top">
    <div class="container px-4">
      <RouterLink class="navbar-brand" to="/">
        <img src="../assets/logo.png" alt="logo de suricata" />
      </RouterLink>
      <button
        class="navbar-toggler navbar-dark border-light"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item active">
            <RouterLink class="nav-link text-light" :to="{ name: 'home' }"
              >Inicio <span class="sr-only">(current)</span></RouterLink
            >
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link text-light" :to="{ name: 'product' }"
              >Productos</RouterLink
            >
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link text-light" :to="{ name: 'contact' }"
              >Contacto</RouterLink
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

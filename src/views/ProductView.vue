<script>
import { RouterLink } from 'vue-router'
import TheCard from '../components/TheCard.vue'
import productData from '../dataList.json'

export default {
  name: 'ProductView',
  components: {
    TheCard
  },
  props: {
    nombre: {
      type: String,
      required: true,
    } ,
    descripcion: {
      type: String,
      required: true,
    },
    precio: {
      type: Number,
      required: true,
    }, 
    cantidad: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      products: productData.products
    }
  }
}
</script>

<template>
  <div class="product">
    <section class="container" id="productos">
      <RouterLink :to="{name: 'home'}"> Inicio </RouterLink>
      
      <h1 class="text-center">Nuestros Productos</h1>
      
      <div class="row">
        <!-- primera con props del router -->
        <div class="col-12 col-md-6 col-lg-4 px-5 mb-4">
          <div class="card">
            <img src="/img/desayunos.jpg" class="card-img-top" alt="desayuno" />
            <div class="card-body">
              <h5 class="card-title fw-bold">{{ nombre }}</h5>
              <p class="card-text">
                {{ descripcion }}
              </p>
            </div>
            <ul class="list-group list-group-flush">
              <li class="list-group-item">Precio: ${{ precio }}</li>
              <li class="list-group-item">Cantidad: {{ cantidad }}</li>
            </ul>
            <div class="card-body">
              <a href="#" class="card-link">Ver más</a>
              <a href="#" class="card-link">Comprar</a>
            </div>
          </div>
        </div>

        <!-- Lista desde Json -->
          <TheCard 
            v-for="product in products" 
            :key="product.id" 
            :nombre="product.nombre" 
            :descripcion="product.descripcion" 
            :img="product.img" 
            :precio="product.precio"
            :cantidad="product.cantidad" 
          />
      </div>
    </section>
  </div>
</template>

<style>

.product {
  margin: 4rem 2rem;
}

</style>

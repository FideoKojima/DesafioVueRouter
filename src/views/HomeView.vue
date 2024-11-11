<script>
  import TheCard from '../components/TheCard.vue'
  import productData from '/src/dataList.json'
  
  export default {
    components: {
      TheCard
    },
    data() {
      return {
        products: productData.products
      }
    },
    computed: {
      limitedProducts() {
        return this.products.slice(0, 3);
      }
    }
  }
</script>

<template>
  <section class="container" id="productos">
    <h1 class=" text-center">Bienvenido a Suricata</h1>

    <h2 class="text-center mb-5">Nuestros Productos Más Populares</h2>
    <div class="row mb-5">
      <TheCard 
        v-for="product in limitedProducts" 
        :key="product.id" 
        :nombre="product.nombre" 
        :descripcion="product.descripcion" 
        :img="product.img" 
        :precio="product.precio"
        :cantidad="product.cantidad" 
      />
    </div>
  </section>
</template>
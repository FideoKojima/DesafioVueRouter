<script>
import { RouterView } from 'vue-router'
import TheNavbar from '@/components/TheNavbar.vue'
import TheFooter from '@/components/TheFooter.vue'
import MediosPago from '@/components/MediosPago.vue'
  
  export default {
    name: 'HomeView',
    components: {
      TheNavbar,
      TheFooter,
      MediosPago
    }
  }
</script>

<template>
  <TheNavbar />

  <RouterView />
  
  <MediosPago/>
  <TheFooter />
</template>


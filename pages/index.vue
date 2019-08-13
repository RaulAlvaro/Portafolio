<template>
  <div>
      <Portrait/>
      <Services/>
      <Portafolio/>
      <SobreMi/>
      <Contacto/>
  </div>
</template>

<script>
import Portrait from '../components/Portrait.vue'
import Services from '../components/Services.vue'
import Portafolio from '../components/Portafolio.vue'
import SobreMi from '../components/SobreMi.vue'
import Contacto from '../components/Contacto.vue'
export default {
  components: {
    Portrait,
    Services,
    SobreMi,
    Portafolio,
    Contacto
  }
}
</script>

<style>

</style>

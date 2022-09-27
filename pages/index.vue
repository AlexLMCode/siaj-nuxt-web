<template>
  <div>
    <p-hero />
    <p-main class="container" />
    <slider />
    <clientes />
    <p-ubicacion class="container" />
    <p-contacto class="container" />
  </div>
</template>

<script>
import PHero from '@/components/PHero';
import PMain from '@/components/PMain';
import PUbicacion from '@/components/PUbicacion';
import PContacto from '@/components/PContacto';
import Slider from '@/components/Slider';
import Clientes from '@/components/Clientes';

// @ is an alias to /src
export default {
  name: 'Home',
  components: {
    PHero,
    PMain,
    PUbicacion,
    PContacto,
    Slider,
    Clientes,
  },
};
</script>

.
<style>
.container {
  width: 85vw;
  margin: auto;
}
</style>

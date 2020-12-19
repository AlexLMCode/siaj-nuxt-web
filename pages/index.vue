<template>
  <div>
    <p-hero />
    <p-main class="container" />
    <slider />
    <p-circles class="container" />
    <clientes />
    <p-ubicacion class="container" />
    <p-contacto class="container" />
  </div>
</template>

<script>
import PHero from '@/components/PHero';
import PMain from '@/components/PMain';
import PCircles from '@/components/PCircles';
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
    PCircles,
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

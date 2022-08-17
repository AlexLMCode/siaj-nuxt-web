<template>
  <div class="carousel-wrapper">
    <div class="carousel-container">
      <VueSlickCarousel v-bind="settings" class="slide-contenedor">
        <div class="item">
          <section class="section slider-quote">
            <p class="section__title">nos recomiendan</p>
            <div class="section__separator"></div>
            <p class="section__description">
              " Me hicieron sentir muy segura y los tramites fueron muy
              rapidos."
              <br />
              <small>Fernanda López. Veracruz,Ver</small>
            </p>
          </section>
          <img src="~/assets/photos/quotes-bg-sebastian-pichler.jpg" alt="" />
        </div>
        <div class="item">
          <section class="section slider-quote">
            <p class="section__title">nos recomiendan</p>
            <div class="section__separator"></div>
            <p class="section__description">
              "Se pusieron en contacto conmigo a la brevedad, siempre atentos de
              mi caso, excelente!"
              <br />
              <small>Roberto Villa. Xalapa, Ver</small>
            </p>
          </section>
          <img src="~/assets/photos/quotes-bg-sebastian-pichler.jpg" alt="" />
        </div>
        <div class="item">
          <section class="section slider-quote">
            <p class="section__title">nos recomiendan</p>
            <div class="section__separator"></div>
            <p class="section__description">
              "Eficientes y eficaces, todo lo que podia esperar."
              <br />
              <small>Rodrigo Saldivar. Ver, Boca del Río</small>
            </p>
          </section>
          <img src="~/assets/photos/quotes-bg-sebastian-pichler.jpg" alt="" />
        </div>
      </VueSlickCarousel>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel';
import 'vue-slick-carousel/dist/vue-slick-carousel.css';
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css';

export default {
  name: 'MyComponent',
  components: { VueSlickCarousel },
  data() {
    return {
      settings: {
        dots: true,
        arrows: true,
        dotsClass: 'slick-dots custom-dot-class',
        edgeFriction: 0.35,
        infinite: false,
        speed: 500,
        slidesToShow: 1,
        slidesToScroll: 1,
      },
    };
  },
};
</script>

<style scoped>
.item {
  display: flex !important;
  justify-content: center;
  align-items: center;
}
.item img {
  height: 40rem;
  width: 100%;
  filter: brightness(50%);
}
.carousel-wrapper {
  width: 100%;
  height: auto;
  margin: 0 auto;
  display: flex;
}

.carousel-container {
  padding: 28px;
  width: 100%;
  height: auto;
}
.slider {
  background-color: green;
  height: 20rem;
  width: 100%;
}
.slide-contenedor {
  position: relative;
}

.slider-quote {
  position: absolute;
  margin: 0;
  color: white;
  z-index: 2;
  max-width: 75vw;
}
</style>

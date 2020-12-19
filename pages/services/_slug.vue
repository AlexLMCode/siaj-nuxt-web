<template>
  <div>
    <header class="header">
      <div class="hero">
        <nav class="hero__nav">
          <figure class="hero__nav__icon">
            <img
              src="~/assets/icons/hamburguer-menu.svg"
              alt="menu"
              @click="toggleMenu"
            />
          </figure>
          <router-link to="/">
            <figure class="hero__nav__logo">
              <img
                src="~/assets/icons/logo-pequeño.svg"
                alt="logo de la empresa"
              />
            </figure>
          </router-link>
          <ul class="hero__menu" :class="{ isActive: menu }">
            <li>
              <NuxtLink to="/#firma">la firma</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/#clientes">clientes</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/#servicios">servicios</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/#ubicacion">ubicacion</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/#contacto">contacto</NuxtLink>
            </li>
          </ul>
        </nav>
      </div>
    </header>
    <main>
      <section class="section__especialidad">
        <div class="section__especialidad__header">
          <p class="section__title">{{ pageInfo.titulo }}</p>
          <div class="section__separator"></div>
        </div>
        <div class="section__especialidad__main">
          <p class="section__especialidad__description">
            {{ pageInfo.descripcion }}
          </p>
          <ul class="section__especialidad__list">
            <li v-for="punto in pageInfo.puntos" :key="punto">
              {{ punto }}
            </li>
          </ul>
        </div>
      </section>
      <div class="section__especialidades__list">
        <div>
          <p class="section__title">especialidades</p>
          <div class="section__separator"></div>
        </div>
        <ul class="section__especialidades__list__container">
          <li>
            <NuxtLink to="/services/mercantil">litigio mercantil</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/services/civil">litigio civil</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/services/administrativo"
              >litigio administrativo
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/services/familiar">litigio familiar</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/services/intelectual"
              >propiedad intelectual
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/services/laboral">litigio laboral</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/services/fiscal">litigio fiscal</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/services/penal">litigio penal</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/services/inmobiliario"
              >litigio inmobiliario
            </NuxtLink>
          </li>
        </ul>
      </div>
    </main>
  </div>
</template>

<script>
import { services } from '~/assets/data/services.json';

export default {
  // eslint-disable-next-line require-await
  async asyncData({ params }) {
    const slug = params.slug; // When calling /abc the slug will be "abc"
    const pageInfo = services[slug];
    return { slug, pageInfo };
  },
  data() {
    return {
      menu: false,
    };
  },
  methods: {
    toggleMenu() {
      this.menu = !this.menu;
    },
  },
};
</script>

<style scoped>
.header {
  width: 100vw;
  height: 8rem;
  position: relative;
  background-color: var(--main-color);
}

.hero {
  position: absolute;
  top: 0;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.hero__container {
  width: 100vw;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
}

.hero__nav {
  margin-top: 2rem;
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  flex-direction: column;
}

.hero__title__logo img {
  width: calc(30rem + 1vw);
}

.hero__nav__icon {
  position: fixed;
  top: 2rem;
  right: 2rem;
  cursor: pointer;
  z-index: 3;
}

.hero__nav__icon img {
  width: 4rem;
}

.hero__menu {
  font-size: 1.6rem;
  display: flex;
  justify-content: space-evenly;
  flex-direction: column;
  align-items: center;
  position: fixed;
  background-color: rgba(165, 161, 123, 0.7);
  z-index: 2;
  top: 0;
  left: 100%;
  width: 100vw;
  height: 100vh;
  transition: 0.3s;
}

.isActive {
  left: 0;
}

.hero__menu li {
  list-style: none;
}

.hero__menu li a {
  color: white;
  font-weight: lighter;
  text-transform: uppercase;
}

/*MAIN*/

main {
  width: 85vw;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}

.section {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: auto;
  margin-top: 5rem;
  margin-bottom: 10rem;
  text-align: center;
}

.section__title {
  font-weight: var(--heading-weight);
  font-size: var(--heading-size);
  text-transform: uppercase;
  margin-bottom: 2rem;
}

.section__separator {
  height: 0.3rem;
  width: 50%;
  background-color: var(--main-color);
  margin-bottom: 2rem;
}

.section__description {
  font-size: 1.6rem;
  text-align: center;
  max-width: 70rem;
}

/*LIST*/

.section__especialidad {
  margin-top: 5rem;
}

.section__especialidades__list {
  width: 100%;
  height: auto;
  background-color: var(--light-gray);
  margin: 5rem 0 5rem 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 1rem;
}

.section__especialidades__list > div {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.section__especialidades__list__container {
  width: 75%;
  height: 35rem;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: flex-start;
  color: var(--main-color);
  font-size: 1.6rem;
  text-transform: uppercase;
}

.section__especialidades__list__container li a {
  text-decoration: none;
  color: inherit;
}

.section__especialidades__list__container li {
  list-style-image: url('~assets/icons/bullet-list-services-smartline.svg');
}

/*ESPECIALIDAD*/

.section__especialidad__main {
  margin-bottom: 5rem;
}

.section__especialidad__header {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.section__especialidad__description {
  color: rgba(0, 0, 0, 0.7);
  font-size: 1.6rem;
  text-align: center;
  margin-bottom: 3rem;
}

.section__especialidad__list {
  font-size: 1.6rem;
  display: flex;
  flex-direction: column;
  width: 75%;
  margin: 0 auto;
}

.section__especialidad__list li {
  list-style-image: url('~assets/icons/list-bullet-Kiranshastry 7.svg');
  margin-bottom: 2rem;
}

.section__especialidad__list li a {
  text-decoration: none;
  color: black;
}

/*FOOTER*/

.footer {
  background-color: #2c2a2b;
}

.footer__container {
  width: 85vw;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.footer__description {
  font-size: 2rem;
  color: white;
  text-transform: uppercase;
  font-weight: 700;
  height: 10rem;
  align-items: center;
  display: flex;
  border-bottom: 1px solid white;
  width: 100%;
  max-width: 80%;
  text-align: center;
  justify-content: center;
}

.footer__logo {
  margin-top: 3rem;
  margin-bottom: 3rem;
}

/*MEDIA QUERIES*/

@media screen and (min-width: 900px) {
  html {
    font-size: 70%;
  }

  .hero__nav__icon {
    display: none;
  }

  .hero__menu {
    display: flex;
    justify-content: space-evenly;
    flex-direction: row;
    align-items: center;
    position: static;
    background-color: initial;
    z-index: 0;
    width: auto;
    height: auto;
  }

  .hero__menu li {
    margin-right: 2rem;
  }

  .hero__nav {
    flex-direction: row;
    width: 90vw;
    margin-right: auto;
    margin-left: auto;
    justify-content: space-between;
  }

  .section__especialidades__list {
    width: 50rem;
  }
}
</style>

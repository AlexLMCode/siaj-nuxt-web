<template>
  <header class="header">
    <div class="background-image"></div>
    <div class="hero">
      <nav ref="nav" class="hero__nav">
        <figure class="hero__nav__icon">
          <img
            src="~/assets/icons/hamburguer-menu.svg"
            alt="menu"
            @click="toggleMenu"
          />
        </figure>
        <a href="/">
          <figure class="hero__nav__logo">
            <img
              src="~/assets/icons/logo-pequeño.svg"
              alt="logo de la empresa"
            />
          </figure>
        </a>
        <ul class="hero__menu" :class="{ isActive: menu }">
          <li>
            <a href="#firma">la firma</a>
          </li>
          <li>
            <a href="#clientes">clientes</a>
          </li>
          <li>
            <a href="#servicios">servicios</a>
          </li>
          <li>
            <a href="#ubicacion">ubicacion</a>
          </li>
          <li>
            <a href="#contacto">contacto</a>
          </li>
        </ul>
      </nav>
      <div ref="hero" class="hero__container">
        <p class="hero__title">LIDERAZGO EN LITIGIO</p>
        <picture class="hero__title__logo">
          <img
            src="~/assets/icons/logo-pequeño-blanco.svg"
            alt="logo de la empresa"
          />
        </picture>
        <a href="#firma">
          <figure class="hero__arrow">
            <img
              src="~/assets/icons/circle-down.svg"
              alt="circulo para bajar"
            />
          </figure>
        </a>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Home',
  components: {},
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
  height: 100vh;
  position: relative;
}

.background-image {
  width: 100%;
  height: 100%;
  background-image: url('~assets/photos/background-large.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
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

.hero__title {
  font-weight: 300;
  color: white;
  font-size: var(--heading-size);
}

.hero__arrow img {
  animation: bounce 1s infinite alternate;
}

@keyframes bounce {
  from {
    transform: translateY(0px);
  }
  to {
    transform: translateY(-15px);
  }
}

@media screen and (min-width: 900px) {
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
}
</style>

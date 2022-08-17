<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__description">
        <p>boca del rio | xalapa | méxico</p>
      </div>
      <figure class="footer__logo">
        <NuxtLink to="/">
          <img
            src="~/assets/icons/logo-pequeño-blanco.svg"
            alt="logo empresa"
          />
        </NuxtLink>
      </figure>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
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
</style>
